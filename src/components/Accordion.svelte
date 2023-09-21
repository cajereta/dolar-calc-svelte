<script>
	import { AccordionItem, Accordion } from 'flowbite-svelte';
</script>

<Accordion class="text-left">
	<AccordionItem>
		<span slot="header" class="text-gray-600 dark:text-gray-200"
			>¿Qué es el dolar tarjeta o turista en Argentina?</span
		>
		<p class="text-gray-700 dark:text-gray-100">
			El dólar tarjeta, también conocido como «dólar turista», es el tipo de
			cambio que se aplica en los consumos de tu tarjeta de crédito en dólares.
			Se trata de una sobretasa del 30% (Impuesto PAIS) que se le agrega al
			precio de lo que cotiza el dólar oficial sumado a la retención 45% por el
			Impuesto a las Ganancias.
		</p>
		<p class="text-gray-700 dark:text-gray-100">
			Además, si los gastos en la tarjeta superan los 300 dólares se suma el
			Impuesto a los Bienes Personales de un 25%.
		</p>
	</AccordionItem>
	<AccordionItem>
		<span slot="header" class="text-gray-600 dark:text-gray-200"
			>¿Qué es el impuesto PAÍS?</span
		>
		<p class="mb-2 text-gray-700 dark:text-gray-100">
			El Impuesto PAIS es un tributo de emergencia establecido en febrero de
			2020 a través de la Ley N° 27.541 de Solidaridad Social y Reactivación
			Productiva en el marco de la Emergencia Pública. Lo recaudado es
			distribuido de la siguiente forma:
		</p>

		<ul class="list-disc pl-5 dark:text-gray-100 text-gray-700">
			<li>70% para financiar programas a cargo de Anses y PAMI.</li>
			<li>
				30% Para financiar obras de vivienda social, del fideicomiso Fondo de
				Integración Sociourbana, prestaciones del PAMI, obras de infraestructura
				económica y fomento del turismo nacional.
			</li>
		</ul>
		<p class="text-gray-700 dark:text-gray-100">
			Para mas información&nbsp;
			<a
				class="text-cyan-600 hover:underline dark:text-cyan-500"
				href="https://www.afip.gob.ar/impuesto-pais/caracteristicas/definicion.asp"
			>
				sobre el impuesto a país haz click aquí
			</a>
			.
		</p>
	</AccordionItem>
	<AccordionItem>
		<span slot="header" class="text-gray-600 dark:text-gray-200">
			¿Qué es el impuesto a las ganancias?</span
		>
		<p class="mb-2 text-gray-700 dark:text-gray-100">
			Es un impuesto nacional que recae sobre los haberes o rentas obtenidos
			durante el año calendario. El mismo se calcula mediante la aplicación de
			una alícuota progresiva sobre la ganancia neta (ingresos menos gastos
			deducibles) obtenida durante el período fiscal de liquidación.
		</p>

		<p class="text-gray-700 dark:text-gray-100">
			Para mas información&nbsp;
			<a
				class="text-cyan-600 hover:underline dark:text-cyan-500"
				href="https://www.afip.gob.ar/gananciasYBienes/ganancias/conceptos-basicos/ganancias.asp"
			>
				sobre el impuesto a las ganancias haz click aquí
			</a>
			.
		</p>
	</AccordionItem>
</Accordion>
