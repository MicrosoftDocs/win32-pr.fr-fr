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
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865841"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




