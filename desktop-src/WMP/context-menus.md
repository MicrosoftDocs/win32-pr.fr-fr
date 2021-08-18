---
title: Menus contextuels
description: Menus contextuels
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Lecteur Windows Media des magasins en ligne, des menus contextuels
- magasins en ligne, menus contextuels
- types 1 magasins en ligne, menus contextuels
- Lecteur Windows Media des magasins en ligne, des menus contextuels personnalisés
- magasins en ligne, menus contextuels personnalisés
- types 1 magasins en ligne, menus contextuels personnalisés
- menus contextuels
- menus contextuels personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ad3bba5863f83b5f324821ec0904e7ef4c5881c7f10b9214eebde1081b217d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119348"
---
# <a name="context-menus"></a>Menus contextuels

Les magasins en ligne peuvent fournir des menus contextuels personnalisés. Pour ce faire, le plug-in du magasin en ligne implémente la méthode [IWMPContentPartner :: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) . Lecteur Windows Media appelle cette méthode pour fournir des informations sur l’emplacement dans l’interface utilisateur où le menu contextuel s’affiche (où l’utilisateur a cliqué avec le bouton droit). Le plug-in retourne un tableau de structures [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) qui décrivent chaque élément de menu contextuel, y compris un ID de commande pour chacun.

une fois que Lecteur Windows Media a récupéré le tableau, le lecteur utilise le tableau pour générer le menu contextuel que l’utilisateur voit. Quand l’utilisateur clique sur un élément dans le menu contextuel, le lecteur appelle [IWMPContentPartner :: commande InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), en passant l’ID de commande associé à l’élément de menu par le biais du paramètre *dwCommandID* . Le lecteur passe également une valeur d’emplacement de bibliothèque et un tableau d’ID qui représente les éléments sur lesquels le menu a été appelé, tel qu’un tableau d’ID de suivi. À l’aide de ces informations, le plug-in peut démarrer tout processus approprié en réponse au clic de la souris de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




