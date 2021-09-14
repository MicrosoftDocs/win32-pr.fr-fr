---
description: Les composants qualifiés sont une méthode d’indirection et peuvent être utilisés pour regrouper des composants avec des fonctionnalités parallèles dans des catégories.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Utilisation des composants qualifiés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222913"
---
# <a name="using-qualified-components"></a>Utilisation des composants qualifiés

Les composants qualifiés sont une méthode d’indirection et peuvent être utilisés pour regrouper des composants avec des fonctionnalités parallèles dans des catégories.

Pour retourner le chemin d’accès complet et installer un [composant qualifié](qualified-components.md), appelez [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).

Pour énumérer tous les qualificateurs de composants qualifiés et les chaînes descriptives, appelez [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

**Pour regrouper des composants dans une catégorie de composants qualifiés**

1.  Il doit y avoir un enregistrement dans la [table](component-table.md) des composants pour chaque composant inclus dans la nouvelle catégorie de composants qualifiés. Créez les champs de la table Component de la même façon que pour les composants ordinaires. Notez que chaque composant qualifié doit avoir un GUID d’ID de composant unique entré dans la colonne ComponentId de la table des composants.
2.  Générez une chaîne de texte de qualificateur pour chaque composant qualifié. Le qualificateur doit être une chaîne de texte unique qui peut être générée facilement lors de la recherche d’un composant qualifié. Par exemple, si les composants de la catégorie sont qualifiés par langue, l’identificateur de paramètres régionaux (LCID) numérique est une chaîne de qualificateur raisonnable.
3.  Ajoutez un enregistrement dans la [table PublishComponent](publishcomponent-table.md) pour chaque composant qualifié. Entrez les identificateurs de composant qualifiés de la colonne composant de la table de composants dans la \_ colonne composant de la table PublishComponent. Entrez les chaînes de qualificateur pour chaque composant qualifié dans la colonne qualificateur. Entrez une chaîne localisée à afficher à l’utilisateur et décrivant le composant qualifié dans la colonne facultative AppData. Une chaîne explicative doit être placée dans le champ AppData, par exemple « dictionnaire français », au lieu du LCID numérique uniquement. Entrez le nom de la fonctionnalité qui utilise ce composant dans la \_ colonne fonctionnalité. L’identificateur de fonctionnalité dans ce champ doit également être listé dans la colonne fonctionnalité du [tableau des fonctionnalités](feature-table.md).
4.  Générez un GUID de catégorie pour cette catégorie de composants qualifiés. Il doit s’agir d’un [GUID](guid.md)valide. Si vous utilisez un utilitaire tel que GUIDGEN pour générer le GUID, assurez-vous qu’il contient uniquement des lettres majuscules. Pour chaque composant qualifié de cette catégorie, entrez le GUID de la catégorie dans le champ ComponentId de la [table PublishComponent](publishcomponent-table.md).

L’exemple suivant montre comment la catégorie « modèles de télécopie » des composants qualifiés est créée dans les tables composant, fonctionnalité et PublishComponent.

[Table PublishComponent](publishcomponent-table.md)



| ComponentId                  | Qualificateur | AppData             | Fonctionnalité\_   | Composant\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {GUID de catégorie de modèle de télécopie} | 1033      | Modèle anglais américain | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Modèle japonais   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | Modèle thaï       | FAXTemplate | FAXTemplateTHA |
|                              | 1031      | Modèle allemand     | FAXTemplate | FAXTemplateDEU |



 

[Table des composants](component-table.md) (table partielle)



| Composant      | ComponentId                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*GUID du composant de modèle de télécopie (anglais des États-Unis)*} |
| FAXTemplateJPN | {*GUID du composant de modèle de télécopie (japonais)*}   |
| FAXTemplateTHA | {*GUID du composant de modèle de télécopie (thaï)*}       |
| FAXTemplateDEU | {*GUID du composant de modèle de télécopie (allemand)*}     |



 

[Table des fonctionnalités](feature-table.md) (table partielle)



| Fonctionnalité     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



