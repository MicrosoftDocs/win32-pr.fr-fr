---
description: Appelé lorsque le certificat retourné par le rappel CertStoreProvFindCert n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: CertStoreProvFreeFindCert fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529346"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>CertStoreProvFreeFindCert fonction de rappel

La fonction de rappel **CertStoreProvFreeFindCert** est appelée lorsque le certificat retourné par le rappel [**CertStoreProvFindCert**](certstoreprovfindcert.md) n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à **CertStoreProvFindCert**. Avant d’appeler le rappel de fermeture, tous les certificats retournés par le rappel [**CertStoreProvFindCert**](certstoreprovfindcert.md) doivent être libérés par le fournisseur à l’aide de **CertStoreProvFindCert** ou **CertStoreProvFreeFindCert**.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
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

*pCertContext* \[ dans\]
</dt> <dd>

Pointeur vers un [**\_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

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

[**contexte du certificat \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
