---
description: Obtient le certificat à partir des informations d’identification de l’utilisateur.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: GetCertificateFromCred, fonction (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531878"
---
# <a name="getcertificatefromcred-function"></a>GetCertificateFromCred fonction)

Obtient le certificat à partir des informations d’identification de l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProviderHandle* \[ dans\]
</dt> <dd>

Descripteur de fournisseur d’identité.

</dd> <dt>

*ClientToken* \[ dans\]
</dt> <dd>

Jeton de l’appelant qui récupère le certificat.

</dd> <dt>

*SuppliedCred* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**\_ \_ d’informations d’identification fournie par SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) qui contient les informations d’identification d’un ID en ligne dont le certificat est demandé. Le fournisseur d’identité doit valider les données d’entrée comme s’il s’agissait d’une source non fiable.

</dd> <dt>

*SuppliedCredSize* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *SuppliedCred* .

</dd> <dt>

*CertContext* \[ à\]
</dt> <dd>

Si la fonction est réussie, ce paramètre est un pointeur vers le pointeur de \_ contexte CCERT retourné. Lorsque vous avez terminé d’utiliser le contexte de certificat, libérez-le en appelant la fonction [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la fonction retourne l’état \_ Success.

Si la fonction échoue, la fonction peut retourner l’un des codes d’erreur NTSTATUS suivants.



| Valeur retournée                                                                                            | Description                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>ÉTAT \_ non \_ pris en charge</dt> </dl>       | Le fournisseur d’identité ne reconnaît pas le type d’informations d’identification des informations d’identification fournies. LSA essaiera le fournisseur d’identité suivant.<br/>                                           |
| <dl> <dt>\_échec d’ouverture de session \_</dt> </dl>       | Les informations d’identification sont incorrectes.<br/>                                                                                                                                                |
| <dl> <dt>paramètre d’état \_ non valide \_</dt> </dl>   | Un paramètre n'est pas valide. Les informations d’identification peuvent être dans un format incorrect et non dans la structure [**\_ \_ d’informations d’identification fournie**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) par le SECPKG défini.<br/> |
| <dl> <dt>ÉTAT \_ réseau \_ inaccessible</dt> </dl> | Le fournisseur d’identité ne peut pas contacter le Cloud pour obtenir le certificat.<br/>                                                                                                   |
| <dl> <dt>\_mot de passe d’état \_ expiré</dt> </dl>    | Le mot de passe du compte a expiré.<br/>                                                                                                                                           |
| <dl> <dt>compte d’état \_ \_ verrouillé \_</dt> </dl> | Le compte a été verrouillé. <br/>                                                                                                                                           |
| <dl> <dt>Autres</dt> </dl>                       | Autres codes d’erreur spécifiques au fournisseur. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Notes

Avant d’extraire le certificat du Cloud, le fournisseur d’identité doit vérifier qu’il existe un certificat valide pour cet utilisateur dans le magasin de certificats « MY » de l’utilisateur. Si un certificat valide existe, le fournisseur doit retourner ce certificat pour éviter tout trafic réseau inutile.

Le fournisseur d’identité peut également mettre en cache le certificat localement tant qu’il est protégé par l’utilisateur actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

