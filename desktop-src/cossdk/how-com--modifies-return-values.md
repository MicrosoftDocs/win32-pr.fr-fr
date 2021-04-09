---
description: Modification des valeurs de retour par COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Modification des valeurs de retour par COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110918"
---
# <a name="how-com-modifies-return-values"></a>Modification des valeurs de retour par COM+

COM+ ne modifie jamais la valeur de retour d’un **HRESULT** qui indique un échec, par exemple e \_ inattendu ou e \_ Fail. Toutefois, lorsqu’un objet utilisant la fonctionnalité COM+ retourne une valeur **HRESULT** indiquant une réussite (telle que s \_ OK, s \_ false ou NOerror), com+ convertit parfois le **HRESULT** en code d’erreur com+ avant de retourner à l’appelant.

Par exemple, lorsqu’une application retourne un \_ OK après avoir appelé [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), si l’objet est la racine d’une transaction dont la validation échoue, la valeur **HRESULT** est convertie en contexte \_ E \_ abandonné.

Lorsque COM+ convertit une valeur **HRESULT** , il efface tous les paramètres de sortie de la méthode. Les références retournées sont libérées et les valeurs des pointeurs d’objets retournés ont la valeur **null**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Isolation des erreurs et stratégie FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Recherche de la source d’une erreur](finding-the-source-of-an-error.md)
</dt> <dt>

[Interprétation des codes d’erreur](interpreting-error-codes.md)
</dt> <dt>

[Stratégies de gestion des erreurs dans COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Dépannage](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



