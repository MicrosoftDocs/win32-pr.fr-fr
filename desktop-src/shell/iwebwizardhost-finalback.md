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
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293347"
---
# <a name="webwizardhostfinalback-method"></a>Méthode WebWizardHost. FinalBack

Accède à la page côté client qui précède immédiatement la page hébergeant les pages HTML côté serveur.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Notes

Lorsque l’Assistant affiche la première page côté serveur et que l’utilisateur clique sur le bouton **précédent** , le serveur appelle **FinalBack** lorsqu’il est informé de cet événement par le gestionnaire d’événements du client.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




