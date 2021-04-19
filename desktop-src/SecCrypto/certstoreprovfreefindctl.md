---
description: Appelé lorsque le certificat retourné par le rappel CertStoreProvFindCTL n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: CertStoreProvFreeFindCTL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524172"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>CertStoreProvFreeFindCTL fonction de rappel

La fonction de rappel **CertStoreProvFreeFindCTL** est appelée lorsque le certificat retourné par le rappel [**CertStoreProvFindCTL**](certstoreprovfindctl.md) n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à **CertStoreProvFindCTL**. Avant d’appeler le rappel de fermeture, tous les certificats retournés par le rappel [**CertStoreProvFindCTL**](certstoreprovfindctl.md) doivent être libérés par le fournisseur à l’aide de **CertStoreProvFindCTL** ou **CertStoreProvFreeFindCTL**.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
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

*pCtlContext* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

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

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**\_contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
