---
description: Représente une collection d’objets d’extension.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Objet NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529978"
---
# <a name="noticenumbers-object"></a>Objet NoticeNumbers

\[L’objet **NoticeNumbers** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Pour plus d’informations, consultez [**qualifier**](qualifier.md).\]

L’objet **NoticeNumbers** représente une collection d’objets d' [**extension**](extension.md) . Chaque objet d' [**extension**](extension.md) représente un numéro d’avis de l’utilisateur.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **NoticeNumbers** est utilisé pour effectuer les tâches suivantes :

-   Récupérez le nombre d’objets d' [**extension**](extension.md) dans la collection.
-   Récupérez un objet d' [**extension**](extension.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **NoticeNumbers** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **NoticeNumbers** a ces propriétés.



| Propriété                                              | Type d’accès          | Description                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](noticenumbers-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).<br/> |
| [**Saut**](noticenumbers-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets d' [**extension**](extension.md) dans la collection.<br/>                                                                                                                                    |
| [**Élément**](noticenumbers-item.md)<br/>         | Lecture seule<br/> | Récupère l’objet d' [**extension**](extension.md) qui représente le numéro d’avis indexé de la collection.<br/> Il s’agit de la propriété par défaut.<br/>                                                            |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **NoticeNumbers** .

L’objet NoticeNumbers est utilisé dans la propriété [**qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
