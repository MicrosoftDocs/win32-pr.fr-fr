---
description: Récupère un nombre spécifié d’octets aléatoires à partir du générateur de nombres aléatoires du système.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218001"
---
# <a name="systemprng-function"></a>SystemPrng fonction)

\[**SystemPrng** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

La fonction **SystemPrng** récupère un nombre spécifié d’octets aléatoires à partir du générateur de nombres aléatoires du système.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbRandomData* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les octets récupérés.

</dd> <dt>

*cbRandomData* \[ dans\]
</dt> <dd>

Nombre d'octets à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne toujours la **valeur true**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista avec les \[ applications de bureau SP1 uniquement\]<br/>                                                                                                                                                                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys sur Windows Server 2008 et Windows Vista avec SP1 ;</dt> <dt>Cng.sys sur Windows 7 et Windows Server 2008 R2</dt> </dl> |



 

 




