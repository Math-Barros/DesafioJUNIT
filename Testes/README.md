import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.Test;

import JulgamentoPrisioneiro.Resposta;

class JulgamentoPrisioneiroTest {

	@Test
	public void testeCalculaPena() {

		JulgamentoPrisioneiro jp = new JulgamentoPrisioneiro();

		Resposta respostaSuspeitoA = Resposta.DELACAO;
		Resposta respostaSuspeitoB = Resposta.DELACAO;

		int penaSuspeitoA = jp.calculaPena(respostaPrisioneiroA, respostaPrisioneiroB);
		int penaSuspeitoB = jp.calculaPena(respostaPrisioneiroB, respostaPrisioneiroA);

	}

}
