---
layout: default
title: AIOTI Testbeds Portfolio
---
<head>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bulma@0.8.2/css/bulma.min.css"
    />
    <link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}" />
    
    <script
      src="https://code.jquery.com/jquery-3.5.0.min.js"
      integrity="sha256-xNzN2a4ltkB44Mc/Jz3pT4iU1cmeR0FkXs4pru/JxaQ="
      crossorigin="anonymous">
    </script>
    <script
      src="https://cdnjs.cloudflare.com/ajax/libs/datatables/1.10.20/js/jquery.dataTables.min.js"
      integrity="sha256-L4cf7m/cgC51e7BFPxQcKZcXryzSju7VYBKJLOKPHvQ="
      crossorigin="anonymous">
      </script>
  </head>

Browse the solutions provided by AIOTI members in the table.




<table id="catalogue" class="display" style="width: 1200px">
	<thead>
		<tr>
			<th></th>
			<th></th>
			<th></th>
			<th></th>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		<!--For loop that iterates over markdown frontmatter in _skus folder-->
      {% for solution in site.solutions %}
      
		<tr>
			<td><b>Name</b></td>
			<td><b>Provider</b></td>
			<td><b>Domains</b></td>
			<td><b>Use-cases</b></td>
			<td><b>Access</b></td>
			<td><b>Testbed stage</b></td>
		</tr>
		<tr>
			<td>
				<strong>
					<a href="{{ solution.testbed_url }}">{{ solution.short_name }}
						<br> {{ solution.name }}
						</a>
					</strong>
				</td>
				<td>
					<a href="{{ solution.testbed_url }}">
						<img src="{{ solution.provider_logo }}" alt="{{ solution.provider }}" width=150/>
						<br>{{ solution.provider}} 
							<br>
								<b>Location:</b> {{ solution.city_country}}
							</a>
						</td>
						<td>{{ solution.domains}}</td>
						<td>{{ solution.use-cases}}</td>
						<td>
							<b>License:</b> {{ solution.license}} 
							<br>
								<b>Access:</b> {{ solution.partner_access}}
								<br>
									<b>Contact:</b> {{ solution.contact}}
								</td>
								<td>{{ solution.testbed_stage}}</td>
							</tr>
							<tr>
								<td colspan="6">
									<strong>Description:</strong> {{ solution.description}}
								</td>
							</tr>
							<tr>
								<td colspan="6">
									<img src="{{ solution.descriptionimage }}" alt="{{ solution.provider }}" width=600px />
								</td>
							</tr>
							<tr>
								<td colspan="3">
									<strong>Concept:</strong> {{ solution.concept}}
								</td>
								<td colspan="3">
									<strong>Technology</strong>: {{ solution.technology}}
								</td>
							</tr>
							<tr>
								<td colspan="3">
									<strong>Hardware</strong> {{ solution.hardware}}
								</td>
								<td colspan="3">
									<strong>Software</strong> {{ solution.software}}
								</td>
							</tr>
							<tr>
								<td colspan="6" bgcolor=black></td>
							</tr>
      {% endfor %}
    
						</tbody>
						<!-- 
    <tfoot><tr><th>Name</th><th>Position</th><th>Description</th></tr></tfoot> -->
					</table>
<br><br>

## Contribute to our Portfolio!

This page is an [open-source project available on GitHub](https://github.com/AIOTIEU/testbeds). Feel free to contribute!

<script>
$(document).ready(function() {
    $('#catalogue').DataTable();
} );
</script>
