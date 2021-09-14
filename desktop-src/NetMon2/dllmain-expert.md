---
description: L’expert implémente la fonction DllMain. Le système d’exploitation appelle DllMain pour obtenir un descripteur d’une instance de l’expert.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Fonction de rappel d’expert DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229667"
---
# <a name="dllmain-expert-callback-function"></a>Fonction de rappel d’expert DllMain

L’expert implémente la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) . Le système d’exploitation appelle **DllMain** pour obtenir un descripteur d’une instance de l’expert.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HINSTANCE* \[ à\]
</dt> <dd>

Handle vers une instance de l’expert.

Si l’expert utilise l’interface utilisateur Moniteur réseau, la valeur *HINSTANCE* doit être stockée dans une variable globale. Cette approche est nécessaire uniquement lorsque la valeur du paramètre *ulReason* est définie sur dll \_ process \_ Attach.

</dd> <dt>

*ulReason* \[ dans\]
</dt> <dd>

Indicateur de la raison pour laquelle la fonction a été appelée. La valeur d' \_ attachement du processus dll \_ (qui s’applique lorsque la dll est chargée pour la première fois) indique que l’expert doit enregistrer la valeur *HINSTANCE* dans une variable globale.

Avec toute autre valeur, tous les appels à la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) peuvent être ignorés. Pour obtenir la liste de tous les indicateurs possibles définis par le système d’exploitation, consultez **DllMain**.

</dd> <dt>

*Reserved* 
</dt> <dd>

Le paramètre n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Le système d’exploitation appelle la fonction d’expert **DllMain** lorsqu’un processus charge ou décharge la dll d’expert. La fonction d’expert **DllMain** doit être exportée uniquement si l’expert dispose d’une interface utilisateur pour l’affichage de la configuration ou des résultats, puis uniquement pour retourner la valeur *HINSTANCE* appropriée.

La fonction d’expert **DllMain** est basée sur la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) de la bibliothèque de liens dynamiques.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Process. h</dt> </dl> |



 

