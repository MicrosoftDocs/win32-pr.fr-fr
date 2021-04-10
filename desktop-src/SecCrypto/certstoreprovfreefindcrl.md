---
description: Appelé lorsque le certificat retourné par le rappel CertStoreProvFindCRL n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: CertStoreProvFreeFindCRL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867169"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>CertStoreProvFreeFindCRL fonction de rappel

La fonction de rappel **CertStoreProvFreeFindCRL** est appelée lorsque le certificat retourné par le rappel [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à **CertStoreProvFindCRL**. Avant d’appeler le rappel de fermeture, tous les certificats retournés par le rappel [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) doivent être libérés par le fournisseur à l’aide de **CertStoreProvFindCRL** ou **CertStoreProvFreeFindCRL**.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hStoreProv* \[ dans\]
</dt> <dd>

Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).

</dd> <dt>

*pCrlContext* \[ dans\]
</dt> <dd>

Pointeur vers un [**\_ contexte de liste de révocation de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

</dd> <dt>

*pvStoreProvFindInfo* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient des informations de recherche.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Toutes les valeurs d’indicateur nécessaires.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**\_contexte CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
