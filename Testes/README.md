import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.Test;

class JulgamentoPrisioneiroTest {

	@Test
	public void testeCalculaPena1() {

		JulgamentoPrisioneiro jp = new JulgamentoPrisioneiro();

		Resposta respostaSuspeitoA = Resposta.DELACAO;
		Resposta respostaSuspeitoB = Resposta.DELACAO;

		int penaSuspeitoA = jp.calculaPena(respostaSuspeitoA, respostaSuspeitoB);
		int penaSuspeitoB = jp.calculaPena(respostaSuspeitoB, respostaSuspeitoA);

		assertEquals(15, penaSuspeitoA);
		assertEquals(15, penaSuspeitoB);

	}

	@Test
	public void testeCalculaPena2() {

		JulgamentoPrisioneiro jp = new JulgamentoPrisioneiro();

		Resposta respostaSuspeitoA = Resposta.DELACAO;
		Resposta respostaSuspeitoB = Resposta.NEGACAO;

		int penaSuspeitoA = jp.calculaPena(respostaSuspeitoA, respostaSuspeitoB);
		int penaSuspeitoB = jp.calculaPena(respostaSuspeitoB, respostaSuspeitoA);

		assertEquals(10, penaSuspeitoA);
		assertEquals(10, penaSuspeitoB);

	}

	@Test
	public void testeCalculaPena3() {

		JulgamentoPrisioneiro jp = new JulgamentoPrisioneiro();

		Resposta respostaSuspeitoA = Resposta.NEGACAO;
		Resposta respostaSuspeitoB = Resposta.DELACAO;

		int penaSuspeitoA = jp.calculaPena(respostaSuspeitoA, respostaSuspeitoB);
		int penaSuspeitoB = jp.calculaPena(respostaSuspeitoB, respostaSuspeitoA);

		assertEquals(10, penaSuspeitoA);
		assertEquals(10, penaSuspeitoB);

	}

	@Test
	public void testeCalculaPena4() {

		JulgamentoPrisioneiro jp = new JulgamentoPrisioneiro();

		Resposta respostaSuspeitoA = Resposta.NEGACAO;
		Resposta respostaSuspeitoB = Resposta.NEGACAO;

		int penaSuspeitoA = jp.calculaPena(respostaSuspeitoA, respostaSuspeitoB);
		int penaSuspeitoB = jp.calculaPena(respostaSuspeitoB, respostaSuspeitoA);

		assertEquals(11, penaSuspeitoA);
		assertEquals(11, penaSuspeitoB);

	}

}
