---
description: Spécifie le type de lien lors de l’analyse ou de l’indexation.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Énumération LINKTYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 16c61f8d92a6f90be0fa4b64ddd9d582987ac0bdf52ca1c596c7db3a7fa4b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463042"
---
# <a name="linktype-enumeration"></a>Énumération LINKTYPE

\[l’énumération **LINKTYPE** est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.\]

Spécifie le type de lien lors de l’analyse ou de l’indexation.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**\_URL LinkType**
</dt> <dd>

Spécifie si le type de lien des URL doit être indexé.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**\_contenu LinkType**
</dt> <dd>

Spécifie si le contenu du lien doit être indexé.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE \_ associées**
</dt> <dd>

Spécifie un lien associé.

</dd> </dl>

## <a name="remarks"></a>Remarques

pour prévisualiser les pièces jointes avec un gestionnaire de protocole tiers sur des ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser les indicateurs **LINKTYPE** et les autres api suivantes : les méthodes [**IItemPreviewerExt :: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) et [**IItemPreviewerExt :: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) , et la structure [**LINKINFO**](-search-linkinfo.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 




