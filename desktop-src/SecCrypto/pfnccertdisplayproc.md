---
description: Fonction de rappel définie par l’utilisateur qui permet à l’appelant de la fonction CryptUIDlgSelectCertificate de gérer l’affichage des certificats que l’utilisateur sélectionne pour afficher.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: PFNCCERTDISPLAYPROC fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a0d78569990874c87082d57045cf8075043c6edccc96b507d2d8dc72a58fb379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978975"
---
# <a name="pfnccertdisplayproc-callback-function"></a>PFNCCERTDISPLAYPROC fonction de rappel

La fonction **PFNCCERTDISPLAYPROC** est une fonction de rappel définie par l’utilisateur qui permet à l’appelant de la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) de gérer l’affichage des certificats que l’utilisateur sélectionne pour afficher.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCertContext* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) qui représente le certificat à afficher.

</dd> <dt>

*hWndSelCertDlg* \[ dans\]
</dt> <dd>

Handle de la boîte de dialogue à partir de laquelle le certificat a été sélectionné pour être affiché.

</dd> <dt>

*pvCallbackData* \[ dans\]
</dt> <dd>

Données supplémentaires utilisées par la fonction de rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** pour indiquer qu’elle gère l’affichage du certificat et que la boîte de dialogue ne doit pas afficher le certificat. Si cette fonction retourne la **valeur false**, la boîte de dialogue affiche le certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 




