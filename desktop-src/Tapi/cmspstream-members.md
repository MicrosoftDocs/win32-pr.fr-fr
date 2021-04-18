---
description: La liste suivante contient les membres CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Membres CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115603"
---
# <a name="cmspstream-members"></a>Membres CMSPStream



| Type de membre                     | Nom                | Description                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                        | \*m \_ pFTM           | Pointeur vers le marshaleur libre de threads.                                                                                                   |
| DWORD                           | m \_ dwState          | État actuel du flux.                                                                                                           |
| HANDLE                          | m \_ hAddress         | Adresse sur laquelle ce flux est utilisé.                                                                                            |
| DWORD                           | m \_ dwMediaType      | [**Type de média**](tapimediatype--constants.md) de ce flux (audio, vidéo, etc.).                                                    |
| DIRECTION du TERMINAL \_             | \_direction m        | [**Direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) de ce flux (entrant ou sortant).                                                         |
| CMSPCallBase                    | \*m \_ pMSPCall       | Pointeur vers l’objet d’appel.                                                                                                                |
| IGraphBuilder                   | \*m \_ pIGraphBuilder | Pointeur vers les interfaces d’objet de graphique.                                                                                                        |
| Appel                   | \*m \_ pIMediaControl | Pointeur vers l’interface de contrôle de média.                                                                                                    |
| CMSPArray <ITTerminal \*> | \_terminaux m        | Liste des terminaux sur le flux.                                                                                                       |
| CMSPCritSection                 | \_verrou m             | Verrou qui protège l’objet de flux. L’objet de flux ne doit jamais acquérir le verrou, puis appeler une méthode MSPCall qui peut être verrouillée. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



