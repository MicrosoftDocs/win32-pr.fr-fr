---
description: Récupère la valeur d’une propriété nommée pour un objet clé de fournisseur SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: SslGetKeyProperty, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520114"
---
# <a name="sslgetkeyproperty-function"></a>SslGetKeyProperty fonction)

La fonction **SslGetKeyProperty** récupère la valeur d’une propriété nommée pour un objet de clé de fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HKEY* \[ dans\]
</dt> <dd>

Handle du fournisseur SSL.

</dd> <dt>

*pszProperty* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom de la propriété à récupérer. Il peut s’agir de l’un des [**identificateurs de propriété de stockage de clés**](key-storage-property-identifiers.md) prédéfinis ou d’un identificateur de propriété personnalisé.

</dd> <dt>

*ppbOutput* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la valeur de la propriété. L’appelant de la fonction doit libérer cette mémoire tampon en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ à\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | L’un des handles fournis n’est pas valide.<br/>    |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | L’un des paramètres fournis n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

