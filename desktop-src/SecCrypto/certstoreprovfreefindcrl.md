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
ms.openlocfilehash: 1bf7e3b2518789bdf3755cefec0dcc27c88642c376cafca039ce5cc20533a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769934"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**\_contexte CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
