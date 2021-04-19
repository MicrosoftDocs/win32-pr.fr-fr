---
description: Télécharge la signature du fichier. cab, vérifie les autorisations associées aux packages et les exécute en fonction de l’authentification.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJavaEX fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541134"
---
# <a name="downloadjavaex-function"></a>DownloadJavaEX fonction)

Télécharge la signature du fichier. cab, vérifie les autorisations associées aux packages et les exécute en fonction de l’authentification.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Réservé* \[ dans\]
</dt> <dd>

Ce paramètre est réservé.

</dd> <dt>

*pProviderData* \[ dans\]
</dt> <dd>

Structure [**de \_ \_ données de fournisseur**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) de chiffre qui contient des données de certificat telles que des autorisations de fichier et de zone.

</dd> <dt>

*pJava* \[ dans\]
</dt> <dd>

Structure [**de \_ \_ fournisseur de stratégies Java**](/previous-versions//bb432350(v=vs.85)) qui contient les données relatives au fournisseur de stratégie.

</dd> <dt>

*pFunctions* \[ dans\]
</dt> <dd>

Structure [**de \_ \_ fonctions du fournisseur**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) de chiffrement qui contient une liste de méthodes pour vérifier des objets de certificat, des signatures et des stratégies finales.

</dd> <dt>

*fCertificate* \[ dans\]
</dt> <dd>

Si un certificat est présent, ce paramètre a la **valeur true**. Sinon, la **valeur est false**.

</dd> <dt>

*pTrust* \[ dans\]
</dt> <dd>

Structure [**d' \_ approbation Java**](/windows/desktop/api/Capi/ns-capi-java_trust) qui contient des informations d’approbation, telles que l’autorisation encodée, la signature de l’encodeur et le code de stratégie de retour authentique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est **S \_ OK**. Dans le cas contraire, la valeur de retour est un code d’erreur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
