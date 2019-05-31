
# Extension OCDS sur la variabilité du montant

> Version 0.1 alpha

[*English below*](#ocds-extension-for-value-variability)

Cette [extension](http://standard.open-contracting.org/latest/fr/schema/conformance_and_extensions/#extensions) au format de données [OCDS](http://standard.open-contracting.org/latest/fr/schema/release/) permet d'exprimer la sémantique du champs `formePrix` du [format réglementaire des données essentielles de la commande publique](https://github.com/etalab/format-commande-publique) et permet l'expression de cette donnée lors de la conversion vers OCDS.

Dans le format réglementaire, la forme du prix peut prendre trois valeurs :

- **Ferme** : le montant du marché ne peut pas changer une fois le marché attribué
- **Révisable** : les parties peuvent renégocier une ou plusieurs fois le montant du marché tout au long de sa durée
- **Ferme et actualisable** : les parties se sont mises d'accord sur l'indexation du montant du marché sur une variable (indice des prix à la consommation, taux de chômage, ou tout autre indicateur). Le montant du marché sera donc régulièrement réévalué.

Cette extension ajoute un champ `valueVariability` au bloc de données `award` (attribution), et les valeurs suivantes sont suggérées pour ce champ :

- `none` (= **Ferme**)
- `renegotiable` (= **Révisable**)
- `indexed` (= **Ferme et actualisable**)

Si ces valeurs ne couvrent pas votre besoin, vous pouvez nous les suggérer en créant un issue.

## Licence

Cette extension est publiée selon les termes de la licence Apache 2.0.

# OCDS extension for value variability

> Version 0.1 alpha

This [OCDS extension](http://standard.open-contracting.org/latest/en/schema/conformance_and_extensions/#extensions) was born from our need (the French government) to express one of the fields of our national open contracting data format in OCDS: "forme du prix", which can be translated to "value variability".

This extension add a `valueVariability` field to the `award` block, and the following values are suggested:

- `none`: the value of the contract cannot change once the contract is signed
- `renegotiable`: the parties can renegotiate one or several times at any time within the duration of the contract
- `indexed`: the parties agreed on a a variable or economic indicator on which the value of the contract is indexed and regularly adjusted

## License

This extension is published according the terms of the Apache 2.0 license.
