---
description: Cette fonction prend l’attribut Origin s’il est présent à partir du jeton d’origine et les définit sur un doublon du jeton qui hérite et retourne le jeton dupliqué.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529112"
---
# <a name="srpinheritoriginclaim-function"></a>srpInheritOriginClaim fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Cette fonction prend l’attribut Origin s’il est présent à partir du jeton d’origine et les définit sur un doublon du jeton qui hérite et retourne le jeton dupliqué. L’appelant peut alors emprunter l’identité du jeton retourné. Cette fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à srpapi.dll.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OriginToken* \[ dans\]
</dt> <dd>

Handle vers le jeton qui est dupliqué et reçoit l’attribut Origin hérité. Ce descripteur doit être ouvert avec le \_ droit d’accès en double du jeton.

</dd> <dt>

*InheritingToken* \[ dans\]
</dt> <dd>

Handle vers le jeton qui est dupliqué et reçoit l’attribut Origin hérité. Ce descripteur doit être ouvert avec le \_ droit d’accès en double du jeton. 

</dd> <dt>

*ResultToken* 
</dt> <dd>

En cas de réussite, reçoit le jeton dupliqué. L’appelant peut l’emprunter pour effectuer des opérations avec l’attribut Origin hérité. L’appelant prend la propriété de ce handle et doit le fermer. 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

