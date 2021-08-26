---
description: Contient les données d’attribut d’un fichier.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: ATTRINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090f2ab58d8bf1eb4e379166086d31389b533712a3df23f987bba1331f990891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103729"
---
# <a name="attrinfo-structure"></a>ATTRINFO, structure

Contient les données d’attribut d’un fichier.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**tAttrID**
</dt> <dd>

Type d'attribut. Consultez [types de balises](tag-types.md).

</dd> <dt>

**dwFlags**
</dt> <dd>

Indicateurs de cet attribut.



| Valeur                                                                                                                                                                                                                                           | Signification                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**Attribut \_ DISPONIBLE**</dt> <dt>0x00000001</dt> </dl> | L’attribut est disponible.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**Attribut \_ ÉCHEC**</dt> <dt>0x00000002</dt> </dl>          | L’appel a échoué, car l’attribut n’est pas disponible.<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

Valeur **QWord** (si le type de balise **est \_ type \_ de balise QWord**).

</dd> <dt>

**dwAttr**
</dt> <dd>

Valeur **DWORD** (si le type de balise **est \_ \_ DWORD type de balise**).

</dd> <dt>

**lpAttr**
</dt> <dd>

Pointeur vers une chaîne (si le type de balise est le **type de balise \_ \_ STRINGREF**).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




