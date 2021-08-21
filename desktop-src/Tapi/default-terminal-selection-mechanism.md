---
description: Le concept de terminal multipiste est encore plus souhaitable pour TAPI de fournir une méthode simplifiée de sélection d’un terminal sur un flux ou des flux. Le mécanisme de sélection par défaut des terminaux est conçu pour résoudre ce.
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: Mécanisme de sélection par défaut des terminaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb295c9ea54b0f8572b3ab87f3c8eb9b33ee10773191e3904070c2618b593175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867416"
---
# <a name="default-terminal-selection-mechanism"></a>Mécanisme de sélection par défaut des terminaux

Le concept de [Terminal multipiste](multitrack-terminals.md) est encore plus souhaitable pour TAPI de fournir une méthode simplifiée de sélection d’un terminal sur un flux ou des flux. Le mécanisme de sélection par défaut des terminaux est conçu pour résoudre ce.

## <a name="selecting-a-terminal-on-a-call"></a>Sélection d’un terminal sur un appel

La fonctionnalité de sélection par défaut des terminaux est fournie via la possibilité de sélectionner un terminal sur un appel.

L' [objet Call](call-object.md) expose une nouvelle interface, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2). L’interface expose les mêmes méthodes que [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), ainsi que trois nouvelles méthodes : [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)et [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).

**ITBasicCallControl2 :: RequestTerminal** crée un terminal, en fonction de la classe terminal, de l’orientation et du type de média. Il examine les listes de terminaux statiques et dynamiques pris en charge pour rechercher et créer le terminal demandé.

[**ITBasicCallControl2 :: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) sélectionne le terminal (ou, dans le cas d’un terminal multipiste, énumère, crée si nécessaire et sélectionne les terminaux de suivi) sur le flux (ou les flux) disponibles sur l’appel.

L’algorithme de correspondance des flux d’appels avec le terminal (ou les pistes disponibles sur le terminal) est décrit dans la documentation de [**ITBasicCallControl2 :: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).

L’appel de [**ITBasicCallControl2 :: UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) provoque la désélection du terminal (une seule piste ou multipiste) de l’appel. Pour plus d’informations, consultez la documentation de la méthode.

## <a name="selecting-a-terminal-on-itstream"></a>Sélection d’un terminal sur ITStream

La sélection d’un terminal à simple suivi sur [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (en appelant [**ITStream :: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)) sélectionne le terminal sur le flux. Il s’agit de la procédure de sélection de terminal TAPI 3 habituelle.

Seuls les terminaux à simple suivi peuvent être sélectionnés sur un flux. La sélection d’un terminal multipiste sur un flux échoue, car le flux ne reconnaît pas le type et la direction du média.

 

 
