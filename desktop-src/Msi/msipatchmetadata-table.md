---
description: la Table MsiPatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer le correctif et utilisé par ajout/suppression de programmes.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Table MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee71e25bf04a39d8d360c5977fad7ec72a8924b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469166"
---
# <a name="msipatchmetadata-table"></a>Table MsiPatchMetadata

la Table MsiPatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer le correctif et utilisé par **ajout/suppression de programmes**.

Les correctifs installés sans ce tableau dans la base de données des correctifs (fichier. msp) ne peuvent pas être supprimés et des informations sont manquantes dans **Ajout/suppression de programmes**. La table doit se trouver dans la base de données du fichier correctif et non dans une transformation dans le correctif.

La table MsiPatchMetadata contient les colonnes suivantes.



| Colonne   | Type                         | Clé : | Nullable |
|----------|------------------------------|-----|----------|
| Company  | [Identificateur](identifier.md) | O   | O        |
| Propriété | [Identificateur](identifier.md) | O   | N        |
| Valeur    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Entreprise
</dt> <dd>

Nom de la société. un champ vide (valeur Null) indique que la ligne contient une des propriétés de métadonnées standard de l’Windows Installer. Pour plus d’informations, consultez la section Notes de cette rubrique.

En ajoutant une ligne à la table et en entrant un nom de société dans ce champ, vous pouvez ajouter n’importe quelle société pour étendre le jeu de propriétés.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Nom d’une propriété de métadonnées.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur de la propriété de métadonnées. La valeur ne peut jamais être null ou une chaîne vide.

</dd> </dl>

## <a name="remarks"></a>Remarques

disponible dans Windows Installer 3,0 et versions ultérieures.

les lignes de la Table MsiPatchMetadata qui contiennent une valeur Null dans le champ CompanyName font référence à l’une des propriétés de métadonnées de Windows Installer standard suivantes.




| Propriété | Description | 
|----------|-------------|
| AllowRemoval | Indique si le correctif est un correctif qui peut être <a href="uninstallable-patches.md">installé</a>. Si le champ de valeur contient 0 (zéro), le correctif ne peut pas être supprimé. Si le champ de valeur contient un (1), le correctif est un correctif qui peut être désinstallé. cette propriété est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . <br /> | 
| ManufacturerName | Nom du fabricant de l’application. | 
| MinorUpdateTargetRTM | Indique que le correctif cible la version RTM du produit ou le correctif de mise à niveau majeur le plus récent. Créez cette propriété facultative dans les correctifs de mise à niveau mineurs qui contiennent des informations de séquencement pour indiquer que le correctif supprime tous les correctifs jusqu’à la version RTM du produit, ou jusqu’au correctif de mise à niveau majeur le plus récent. cette propriété est disponible dans Windows Installer 3,1 et versions ultérieures. <br /> | 
| TargetProductName | Nom de l’application ou de la suite d’applications cible. | 
| MoreInfoURL | URL qui fournit des informations spécifiques à ce correctif. Cette propriété est enregistrée et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . à partir de Windows XP avec Service Pack 2 (SP2), cette valeur peut être le lien de support pour le correctif affiché dans <strong>ajout/suppression de programmes</strong>.<br /> | 
| CreationTimeUTC | Heure de création du fichier. msp sous la forme mm-jj-aa HH : MM (mois-jour-année heure : minute). | 
| DisplayName | Titre du correctif logiciel qui est OK pour un affichage public. Cette propriété est enregistrée et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . à partir de Windows XP avec SP2, cette valeur est le nom du correctif qui est affiché dans <strong>ajout/suppression de programmes</strong>.<br /> | 
| Description | Brève description du correctif. | 
| classification ; | Valeur de chaîne qui contient la catégorie arbitraire des mises à jour telles que définies par l’auteur du correctif. Par exemple, les auteurs de correctifs peuvent spécifier que chaque correctif soit classé comme un correctif, un correctif cumulatif de sécurité, une mise à jour critique, une mise à jour, un service pack ou un correctif cumulatif. Cette propriété est obligatoire. | 
| OptimizeCA | indique si le Windows Installer doit ignorer les actions personnalisées lors de l’application du correctif. Cela peut réduire le temps nécessaire pour appliquer le correctif. La propriété OptimizeCA peut avoir l’une des valeurs suivantes :<br /><ul><li>0-ne pas ignorer les actions personnalisées.</li><li>1-ignorer les actions personnalisées d’affectation de répertoire et de propriété. Le <a href="custom-action-type-35.md">type d’action personnalisé 35</a> et le type d' <a href="custom-action-type-51.md">action personnalisé 51</a> peuvent être des actions personnalisées de propriété et d’assignation de répertoire.</li><li>2-ignorer les actions personnalisées immédiates qui ne se trouvent pas dans les assignations de propriété ou de répertoire. Les actions personnalisées immédiates n’incluent pas l’option msidbCustomActionTypeInScript dans la colonne type de la <a href="customaction-table.md">table CustomAction</a>.</li><li>4-ignorer les actions personnalisées qui s’exécutent dans le script.</li></ul>La valeur de OptimizeCA doit être la même pour tous les correctifs en cours d’installation ou aucune action personnalisée n’est ignorée. Par exemple, si deux correctifs sont installés et que OptimizeCA est défini sur les valeurs 1 et 2, aucune action personnalisée n’est ignorée. <br /> Les valeurs de OptimizeCA peuvent être combinées lors du traitement de plusieurs nouveaux correctifs. Si tous les correctifs ont 1 (un) inclus dans les valeurs, toutes les actions personnalisées d’affectation de répertoire et de propriété sont ignorées. Si un correctif a la valeur 3 (trois) pour la propriété et que l’un des correctifs a la valeur 1 (un) pour la propriété, les actions personnalisées d’affectation de répertoire et de propriété sont ignorées. Toutefois, les autres actions personnalisées immédiates s’exécutent, car tous les correctifs demandés ne sont pas ignorés. <br /> | 
| OptimizedInstallMode | Si cette propriété a la valeur 1 (un) dans tous les correctifs à appliquer dans une transaction, une application du correctif est optimisée si possible. Pour plus d’informations, consultez <a href="patch-optimization.md">optimisation des correctifs</a>. disponible à partir de Windows Installer 3,1. | 




 

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




