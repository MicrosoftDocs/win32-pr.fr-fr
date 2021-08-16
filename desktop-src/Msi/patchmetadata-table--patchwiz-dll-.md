---
description: la Table PatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer un correctif et utilisé par ajout/suppression de programmes.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Table PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5845bc279094a4a0280aa1e5e46d161c2d82b4e4037903f502230f6c6d54dca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926149"
---
# <a name="patchmetadata-table-patchwizdll"></a>Table PatchMetadata (PATCHWIZ.DLL)

la Table PatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer un correctif et utilisé par ajout/suppression de programmes. Toutes les propriétés de la table PatchMetadata sont ajoutées à la [table MsiPatchMetadata](msipatchmetadata-table.md) du fichier. msp pour un correctif.

La table PatchMetadata est requise dans les fichiers de propriétés de création de correctifs (fichiers. PCP) qui ont un MinimumRequiredMsiVersion égal à 300 dans le [tableau des propriétés](properties-table-patchwiz-dll-.md). La table est facultative si MinimumRequiredMsiVersion n’est pas égal à 300.

La table PatchMetadata contient les colonnes suivantes.



| Colonne   | Type | Clé | Nullable |
|----------|------|-----|----------|
| Company  | text | O   | O        |
| Propriété | text | O   | N        |
| Valeur    | text |     | O        |



 

### <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Entreprise
</dt> <dd>

Nom de la société. Un champ vide (valeur null) indique que cette ligne contient une des propriétés de métadonnées standard. Une société peut étendre le jeu de propriétés en ajoutant une ligne à la table et en entrant un nom de société dans ce champ.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Nom d’une propriété de métadonnées. Les propriétés AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, description et classification sont requises dans la table PatchMetadata. Ce champ doit contenir l’une des propriétés de métadonnées standard suivantes si le champ Company est vide (valeur null).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowRemoval</td>
<td>Valeur entière qui indique si le correctif logiciel est un correctif pouvant être <a href="uninstallable-patches.md">installé</a>. Si le champ de valeur contient un 0 (zéro), le correctif ne peut pas être supprimé. Si le champ valeur contient 1 (un), le correctif est un correctif qui peut être désinstallé. Cette propriété est obligatoire. Cette propriété est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Valeur de chaîne qui contient le nom du fabricant de l’application. Cette propriété est obligatoire.</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>Indique que le correctif cible la version RTM du produit ou le correctif de mise à niveau majeur le plus récent. Créez cette propriété facultative dans les correctifs de mise à niveau mineurs qui contiennent des informations de séquencement pour indiquer que le correctif supprime tous les correctifs jusqu’à la version RTM du produit, ou jusqu’au correctif de mise à niveau majeur le plus récent. cette propriété est disponible à partir de Windows Installer 3,1.
<blockquote>
[!Note]<br />
pour exiger que Windows Installer 3,1 soit installé pour appliquer le correctif, affectez à la propriété MinimumRequiredMsiVersion la valeur 310 dans la <a href="properties-table-patchwiz-dll-.md">Table des propriétés</a> du fichier. pcp.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>Valeur de chaîne qui contient le nom de l’application ou de la suite d’applications cible. Cette propriété est obligatoire.</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>Valeur de chaîne qui contient une URL pointant vers les informations de ce correctif. Cette propriété requise est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . à partir de Windows XP avec Service Pack 2 (SP2), cette valeur peut être le lien de support pour le correctif affiché dans ajout/suppression de programmes.<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>Valeur de chaîne qui contient l’heure de création du fichier. msp au format mm-jj-aa HH : MM (mois-jour-année heure : minute). Cette propriété est facultative.</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Valeur de chaîne qui contient le titre du correctif logiciel qui est adapté à un affichage public. Cette propriété est obligatoire. Cette propriété est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . à partir de Windows XP avec sp2, cette valeur est le nom du correctif affiché dans ajout/suppression de programmes à partir de Windows XP avec sp2.<br/></td>
</tr>
<tr class="even">
<td>Description</td>
<td>Valeur de chaîne qui contient une brève description du correctif. Cette propriété est obligatoire.</td>
</tr>
<tr class="odd">
<td>Classification</td>
<td>Valeur de chaîne qui contient la catégorie arbitraire des mises à jour telles que définies par l’auteur du correctif. Par exemple, les auteurs de correctifs peuvent spécifier que chaque correctif soit classé comme un correctif, un correctif cumulatif de sécurité, une mise à jour critique, une mise à jour, un service pack ou un correctif cumulatif. Cette propriété est obligatoire.</td>
</tr>
<tr class="even">
<td>OptimizedInstallMode</td>
<td>Si cette propriété a la valeur 1 (un) dans tous les correctifs à appliquer dans une transaction, l’application du correctif logiciel est optimisée si possible. Pour plus d’informations, consultez <a href="patch-optimization.md">optimisation des correctifs</a>. disponible à partir de Windows Installer 3,1.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur de la propriété de métadonnées. La valeur ne peut jamais être null ou une chaîne vide. Cette valeur peut être localisée.

</dd> </dl>

### <a name="remarks"></a>Remarques

disponible à partir de Windows Installer 3,0.

Toutes les propriétés créées dans la table PatchMetadata sont ajoutées à la table MsiPatchMetadata du fichier MSP. Les propriétés AllowRemoval, MoreInfoURL et DisplayName sont inscrites et sont accessibles par le biais de [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

 

 




