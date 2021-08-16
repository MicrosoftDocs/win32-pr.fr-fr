---
description: Stocke des informations sur les types de liens et est utilisé par l’interface IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: LINKINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97c106a5a819ac1068501c77555f3eae238c935e2262894c6c250dfc6782188f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863942"
---
# <a name="linkinfo-structure"></a>LINKINFO, structure

\[**LINKINFO** et [**IItemPreviewerExt**](-search-iitempreviewerext.md) sont pris en charge uniquement sur Windows XP et Windows Server 2003 et ne doivent plus être utilisés.\]

Stocke des informations sur les types de liens et est utilisé par l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**type**
</dt> <dd>

Type : **[ **LinkType**](-search-linktype.md)**

</dd> <dd>

Type de lien spécifié lors de l’analyse ou de l’indexation indiqué par une constante [**LinkType**](-search-linktype.md) .

</dd> <dt>

**bstrContentType**
</dt> <dd>

Type : **BSTR**

</dd> <dd>

Valeur **BSTR** qui spécifie le type de contenu.

</dd> <dt>

**bstrEncoding**
</dt> <dd>

Type : **BSTR**

</dd> <dd>

Attribut EncodingStyle spécifié dans le fichier Web Services Description Language (WSDL).

</dd> <dt>

**bstrFileExt**
</dt> <dd>

Type : **BSTR**

</dd> <dd>

Valeur **BSTR** qui spécifie l’extension de nom de fichier.

</dd> <dt>

**varData**
</dt> <dd>

Type : **variante**

</dd> <dd>

Variant qui spécifie la valeur de la variable.

</dd> <dt>

**dwRelatedParts**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

**Valeur DWORD** qui spécifie les parties associées.

</dd> <dt>

**bstrRelatedCid**
</dt> <dd>

Type : **BSTR**

</dd> <dd>

Valeur **BSTR** qui spécifie une propriété CID, une chaîne décimale non complétée et signée.

</dd> <dt>

**lCodePage**
</dt> <dd>

Type : **long**

</dd> <dd>

Page de codes à utiliser pour l’encodage de la chaîne.

</dd> </dl>

## <a name="remarks"></a>Remarques

pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser la structure **LINKINFO** et les api suivantes : les méthodes [**IItemPreviewerExt :: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) et [**IItemPreviewerExt :: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) et l’énumération [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 




