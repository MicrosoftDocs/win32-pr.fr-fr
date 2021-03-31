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
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203827"
---
# <a name="webwizardhostfinalnext-method"></a>Méthode WebWizardHost. FinalNext

Accède à la page de l’Assistant côté client qui suit la page qui héberge les pages HTML côté serveur, ou termine l’Assistant s’il n’y a pas d’autres pages côté client.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Notes

Lorsque l’Assistant affiche la dernière page HTML côté serveur et que l’utilisateur clique sur le bouton **suivant** ou **Terminer** , le serveur appelle **FinalNext** dans le gestionnaire d’événements de ce bouton.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




