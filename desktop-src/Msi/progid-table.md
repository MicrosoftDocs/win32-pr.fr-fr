---
description: La table ProgId contient des informations sur les ID de programme et les ID de programme indépendants de version qui doivent être générés dans le cadre de la publication du produit.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Table ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed8baea9bd8421757cf2e31f0ba06679db3394c95f732537a7e230c02b5ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042059"
---
# <a name="progid-table"></a>Table ProgId

La table ProgId contient des informations sur les ID de programme et les ID de programme indépendants de version qui doivent être générés dans le cadre de la publication du produit.

La table ProgId contient les colonnes suivantes.



| Colonne         | Type                         | Clé | Nullable |
|----------------|------------------------------|-----|----------|
| ProgId         | [Text](text.md)             | O   | N        |
| ProgId \_ parent | [Text](text.md)             | N   | O        |
| Classe\_        | [GUID](guid.md)             | N   | O        |
| Description    | [Text](text.md)             | N   | O        |
| Située\_         | [Identificateur](identifier.md) | N   | O        |
| IndexIcône      | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId
</dt> <dd>

ID de programme ou ID de programme indépendant de la version. Les ProgID répertoriés dans la table ProgId sont enregistrés si le CLSID répertorié dans la \_ colonne de classe de ce tableau est planifié pour être publié ou installé. Lorsque le ProgId est sélectionné pour l’inscription, tous les ProgID qui font référence à cette ligne par le biais de la \_ colonne parente ProgID sont également sélectionnés pour l’inscription.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ parent
</dt> <dd>

Défini uniquement pour les ID de programme indépendants de la version. Ce champ est une clé étrangère dans la colonne ProgId. Pour définir un ID de programme indépendant de la version, entrez le ProgId correspondant dans la \_ colonne parente ProgID. Lorsque le ProgId est sélectionné pour l’installation, les ProgID indépendants de la version associés à la \_ colonne parente ProgID sont également sélectionnés pour l’inscription.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Type\_
</dt> <dd>

Clé étrangère facultative dans la [table de classe](class-table.md). Cette colonne doit avoir la valeur null pour un ProgId indépendant de la version. Si la \_ valeur de classe d’un ProgID est null, le ProgID est inscrit lorsqu’il apparaît dans la colonne ProgID d’une ligne dans la [table d’extension](extension-table.md) et qu’au moins un verbe est associé à l’extension dans la table de [verbes](verb-table.md). Les ProgID sélectionnés pour l’inscription de cette manière n’installent pas les autres ProgID qui référencent le ProgId actuel via la \_ valeur ProgID par défaut.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description localisée facultative de l’ID de programme associé.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Située\_
</dt> <dd>

Une clé étrangère facultative dans la [table d’icônes](icon-table.md) qui spécifie le fichier d’icône associé à ce ProgID. Il est écrit sous la clé DefaultIcon associée à ce ProgId. Cette colonne doit avoir la valeur null pour un ProgId indépendant de la version.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IndexIcône
</dt> <dd>

Index d’icône dans le fichier d’icône. Cette colonne doit avoir la valeur null pour un ProgId indépendant de la version.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les actions [RegisterProgIdInfo](registerprogidinfo-action.md) et [UnregisterProgIdInfo](unregisterprogidinfo-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



