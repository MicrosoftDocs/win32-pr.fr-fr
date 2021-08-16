---
description: Récupère la valeur d’une propriété de fournisseur spécifiée.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: SslGetProviderProperty, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bfe65fe4033397fd5885eceb3bf0d2ac9ce9aa9b487a84ab7611cb253d979220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906107"
---
# <a name="sslgetproviderproperty-function"></a>SslGetProviderProperty fonction)

La fonction **SslGetProviderProperty** récupère la valeur d’une propriété de fournisseur spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle du fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ) pour lequel la propriété doit être récupérée.

</dd> <dt>

*pszProperty* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom de la propriété à récupérer.

</dd> <dt>

*ppbOutput* \[ à\]
</dt> <dd>

Adresse d’une mémoire tampon qui reçoit la valeur de la propriété.

L’appelant de la fonction doit libérer cette mémoire tampon en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ à\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Adresse d’un pointeur **void** qui reçoit les informations d’état d’énumération utilisées dans les appels ultérieurs à cette fonction. Ces informations n’ont qu’une signification pour le fournisseur SSL et sont opaques pour l’appelant. Le fournisseur SSL utilise ces informations pour déterminer l’élément qui est ensuite dans l’énumération. Si la variable vers laquelle pointe ce paramètre contient la **valeur null**, l’énumération est démarrée à partir du début.

L’appelant de la fonction doit libérer cette mémoire en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le descripteur *hSslProvider* n’est pas valide.<br/>                       |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | L’un des paramètres fournis n’est pas valide.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

