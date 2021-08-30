---
description: La table de mise à niveau contient les informations requises lors des mises à niveau majeures.
ms.assetid: f5fda405-8a09-495e-aa8c-b808a2f02b0f
title: Mettre à niveau la table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3085de7bb834e907ce7b5f1edbee388f5e48b5f72489954aacf3d9e85c2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039189"
---
# <a name="upgrade-table"></a>Mettre à niveau la table

La table de mise à niveau contient les informations requises lors des [mises à niveau majeures](major-upgrades.md). Pour activer pleinement les fonctionnalités de mise à niveau du programme d’installation, chaque package doit avoir une propriété [**UpgradeCode**](upgradecode.md) et une table de mise à niveau. Chaque enregistrement de la table de mise à niveau donne une combinaison caractéristique du code de mise à niveau, de la version du produit et des informations de langue utilisées pour identifier un ensemble de produits affectés par la mise à niveau. Lorsque l’action [FindRelatedProducts](findrelatedproducts-action.md) détecte un produit affecté installé sur le système, il ajoute le code de produit à une propriété spécifiée dans la colonne ActionProperty. L’action [RemoveExistingProducts](removeexistingproducts-action.md) et l’action [MigrateFeatureStates](migratefeaturestates-action.md) suppriment ou migrent uniquement les produits listés dans la colonne ActionProperty.

La table de mise à niveau contient les colonnes indiquées dans le tableau suivant.



| Colonne         | Type                         | Clé | Nullable |
|----------------|------------------------------|-----|----------|
| UpgradeCode    | [GUID](guid.md)             | O   | N        |
| VersionMin     | [Text](text.md)             | O   | O        |
| VersionMax     | [Text](text.md)             | O   | O        |
| Langage       | [Text](text.md)             | O   | O        |
| Attributs     | [Integer](integer.md)       | O   | N        |
| Supprimer         | [Correct](formatted.md)   | N   | O        |
| ActionProperty | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode
</dt> <dd>

La propriété [UpgradeCode](upgradecode.md) dans cette colonne spécifie le code de mise à niveau de tous les produits qui doivent être détectés par l’action [FindRelatedProducts](findrelatedproducts-action.md) .

</dd> <dt>

<span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>VersionMin
</dt> <dd>

Limite inférieure de la plage de versions de produit détectée par [FindRelatedProducts](findrelatedproducts-action.md). Entrez **msidbUpgradeAttributesVersionMinInclusive** dans attributs pour inclure VersionMin dans la plage. Si VersionMin est égal à une chaîne vide (""), elle est évaluée de la même façon que 0. Si VersionMin a la valeur null, FindRelatedProducts ignore **msidbUpgradeAttributesVersionMinInclusive** et détecte toutes les versions précédentes. VersionMin et VersionMax ne doivent pas être tous les deux null.

VersionMin doit être une version de produit valide, comme décrit pour la propriété [**ProductVersion**](productversion.md) . notez que Windows Installer utilise uniquement les trois premiers champs de la version du produit. Si vous incluez un quatrième champ dans la version de votre produit, le programme d’installation ignore le quatrième champ.

</dd> <dt>

<span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>VersionMax
</dt> <dd>

Limite supérieure de la plage de versions de produit détectée par l’action [FindRelatedProducts](findrelatedproducts-action.md) . Entrez **msidbUpgradeAttributesVersionMaxInclusive** dans attributs pour inclure VersionMax dans la plage. Si VersionMax est une chaîne vide (""), elle est évaluée de la même façon que 0. Si VersionMax a la valeur null, FindRelatedProducts ignore **msidbUpgradeAttributesVersionMaxInclusive** et détecte toutes les versions de produit supérieures à (ou supérieures ou égales à) la limite inférieure spécifiée par VersionMin et **msidbUpgradeAttributesVersionMinInclusive**. VersionMin et VersionMax ne doivent pas être tous les deux null.

VersionMax doit être une version de produit valide, comme décrit pour la propriété [**ProductVersion**](productversion.md) . notez que Windows Installer utilise uniquement les trois premiers champs de la version du produit. Si vous incluez un quatrième champ dans la version de votre produit, le programme d’installation ignore le quatrième champ.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous
</dt> <dd>

Ensemble des langues détectées par [FindRelatedProducts](findrelatedproducts-action.md). Entrez une liste d’identificateurs de langue numériques (LANGID) séparés par des virgules. Entrez **msidbUpgradeAttributesLanguagesExclusive** dans attributs pour détecter toutes les langues qui ne sont pas disponibles dans la langue. Si Language a la valeur null ou est une chaîne vide (""), FindRelatedProducts ignore **msidbUpgradeAttributesLanguagesExclusive** et détecte toutes les langues.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Cette colonne contient des indicateurs binaires spécifiant les attributs de la table de mise à niveau.



| Nom de l’indicateur de bit                                 | Decimal | Valeur hexadécimale | Attribut                                                                                                            |
|-----------------------------------------------|---------|-------------|----------------------------------------------------------------------------------------------------------------------|
| **msidbUpgradeAttributesMigrateFeatures**     | 1       | 0x001       | Migre les États de fonctionnalité en activant la logique dans l’action [MigrateFeatureStates](migratefeaturestates-action.md) . |
| **msidbUpgradeAttributesOnlyDetect**          | 2       | 0x002       | Détecte les produits et les applications, mais ne les supprime pas.                                                               |
| **msidbUpgradeAttributesIgnoreRemoveFailure** | 4       | 0x004       | Continue l’installation en cas d’échec de suppression d’un produit ou d’une application.                                              |
| **msidbUpgradeAttributesVersionMinInclusive** | 256     | 0x100       | Détecte la plage de versions, y compris la valeur dans VersionMin.                                                     |
| **msidbUpgradeAttributesVersionMaxInclusive** | 512     | 0x200       | Détecte la plage de versions, y compris la valeur dans VersionMax.                                                     |
| **msidbUpgradeAttributesLanguagesExclusive**  | 1 024    | 0x400       | Détecte toutes les langues, à l’exclusion des langues figurant dans la colonne langue.                                        |



 

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>Installez
</dt> <dd>

Le programme d’installation définit la propriété [**Remove**](remove.md) sur les fonctionnalités spécifiées dans cette colonne. Les fonctionnalités à supprimer peuvent être déterminées au moment de l’exécution. La chaîne [mise en forme](formatted.md) entrée dans ce champ doit correspondre à une liste de noms de fonctionnalités délimitée par des virgules. Par exemple : \[ Feature1 \] , \[ feature2 \] , \[ Feature3 \] . Aucune fonctionnalité n’est supprimée si le champ contient du texte mis en forme qui prend la valeur d’une chaîne vide (""). Le programme d’installation définit REMOVE = ALL uniquement si le champ Remove est vide. Notez la différence entre une chaîne vide et un champ vide. Si le champ est vide, la valeur est null.

</dd> <dt>

<span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>ActionProperty
</dt> <dd>

Lorsque l’action [FindRelatedProducts](findrelatedproducts-action.md) détecte un produit associé installé sur le système, il ajoute le code du produit à la propriété spécifiée dans ce champ. La propriété spécifiée dans cette colonne doit être une propriété publique et l’auteur du package doit ajouter la propriété à la propriété [**SecureCustomProperties**](securecustomproperties.md) . Chaque ligne de la table de mise à niveau doit avoir une valeur ActionProperty unique. Après FindRelatedProducts, la valeur de cette propriété est une liste de codes de produit, séparés par des points-virgules (;), détectés sur le système.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE61](ice61.md)  
[ICE66](ice66.md)  
</dl>

 

 



