---
description: Génère un ensemble de clés de session de protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: SslGenerateSessionKeys, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531227"
---
# <a name="sslgeneratesessionkeys-function"></a>SslGenerateSessionKeys fonction)

La fonction **SslGenerateSessionKeys** génère un ensemble de clés de session de [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*hMasterKey* \[ dans\]
</dt> <dd>

Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*phReadKey* \[ à\]
</dt> <dd>

Pointeur vers le handle de la clé de lecture retournée.

</dd> <dt>

*phWriteKey* \[ à\]
</dt> <dd>

Pointeur vers le handle de clé d’écriture retourné.

</dd> <dt>

*pParameterList* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de mémoires tampons [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) qui contiennent des informations utilisées dans le cadre de l’opération d’échange de clés. L’ensemble précis de mémoires tampons dépend du protocole et de la suite de chiffrement utilisés. Au minimum, la liste contient des mémoires tampons qui contiennent les valeurs aléatoires fournies par le client et le serveur.

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
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | L’un des handles fournis n’est pas valide.<br/>                     |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *phReadKey* ou *phWriteKey* a la valeur null.<br/>            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

