---
description: Accède à la page de l’Assistant côté client qui suit la page qui héberge les pages HTML côté serveur, ou termine l’Assistant s’il n’y a pas d’autres pages côté client.
title: Méthode WebWizardHost. FinalNext (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: a694ced28663a005bfdacd406adb3f6b3d6cd0300db2a101c9fdee4bf215a23d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821119"
---
# <a name="webwizardhostfinalnext-method"></a>Méthode WebWizardHost. FinalNext

Accède à la page de l’Assistant côté client qui suit la page qui héberge les pages HTML côté serveur, ou termine l’Assistant s’il n’y a pas d’autres pages côté client.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Lorsque l’Assistant affiche la dernière page HTML côté serveur et que l’utilisateur clique sur le bouton **suivant** ou **Terminer** , le serveur appelle **FinalNext** dans le gestionnaire d’événements de ce bouton.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




