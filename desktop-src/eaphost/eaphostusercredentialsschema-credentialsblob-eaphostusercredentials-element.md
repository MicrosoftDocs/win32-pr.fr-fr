---
title: Élément CredentialsBlob (EapHostUserCredentials)
description: Est utilisé lorsque la configuration de la méthode est un objet BLOB binaire au lieu du format texte XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Élément CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519624"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Élément CredentialsBlob (EapHostUserCredentials)

L’élément **CredentialsBlob (EapHostUserCredentials)** est utilisé lorsque la configuration de la méthode est un objet blob binaire au lieu du format texte XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

L’élément **CredentialsBlob** est défini par l’élément [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .

## <a name="remarks"></a>Notes

Les [**informations d’identification**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) et les éléments **CredentialsBlob** ne peuvent pas être utilisés simultanément.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





