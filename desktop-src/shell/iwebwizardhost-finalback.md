---
description: Accède à la page côté client qui précède immédiatement la page hébergeant les pages HTML côté serveur.
title: Méthode WebWizardHost. FinalBack (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 0338b20023fda059a5205c9a42a7b7d669c5554d5fca878fcb8904c807ceceae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092606"
---
# <a name="webwizardhostfinalback-method"></a>Méthode WebWizardHost. FinalBack

Accède à la page côté client qui précède immédiatement la page hébergeant les pages HTML côté serveur.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Lorsque l’Assistant affiche la première page côté serveur et que l’utilisateur clique sur le bouton **précédent** , le serveur appelle **FinalBack** lorsqu’il est informé de cet événement par le gestionnaire d’événements du client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




