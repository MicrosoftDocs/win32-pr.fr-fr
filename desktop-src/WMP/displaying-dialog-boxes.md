---
title: Afficher des boîtes de dialogue
description: Afficher des boîtes de dialogue
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Lecteur Windows Media des magasins en ligne, affichage des boîtes de dialogue
- magasins en ligne, afficher des boîtes de dialogue
- types 1 magasins en ligne, affichage des boîtes de dialogue
- Lecteur Windows Media des magasins en ligne, boîtes de dialogue
- magasins en ligne, boîtes de dialogue
- tapez 1 magasins en ligne, boîtes de dialogue
- afficher des boîtes de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e71d177e7675822b1f2704bf62776e598c2e817d583020b0df962347dac4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997269"
---
# <a name="displaying-dialog-boxes"></a>Afficher des boîtes de dialogue

le magasin en ligne peut appeler des boîtes de dialogue par le biais de Lecteur Windows Media. Pour ce faire, appelez [External. ShowPopup](external-showpopup.md) à partir du code de script de la page de découverte, en fournissant une valeur d’index personnalisée qui représente la boîte de dialogue à afficher. Cette valeur d’index n’a de sens que dans le code de la Banque en ligne ; Lecteur Windows Media n’interprète pas cette valeur. Lecteur Windows Media appelle ensuite [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), en passant g \_ szItemInfo \_ PopupURL pour le paramètre *bstrInfoName* et le numéro d’index pour le paramètre *pContext* . Le plug-in retourne alors un **BSTR** contenant l’URL de la page Web à afficher dans la boîte de dialogue et le lecteur affiche la boîte de dialogue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




