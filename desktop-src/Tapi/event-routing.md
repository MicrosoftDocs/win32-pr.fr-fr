---
description: Avec la fonction lineSetTerminal, l’application peut contrôler ou supprimer le routage d’événements de bas niveau spécifiés (échangés entre le commutateur et la station) sur un appareil.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Routage d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6749969faf89ac0212c19049fe02c9dad57a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514024"
---
# <a name="event-routing"></a>Routage d’événements

Avec la fonction [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) , l’application peut contrôler ou supprimer le routage d’événements de bas niveau spécifiés (échangés entre le commutateur et la station) sur un appareil. Avec **lineSetTerminal**, l’application spécifie le périphérique terminal auquel ces événements (tels que Line, Address ou Call Media-Stream Events) sont routés.

Le routage des différentes classes d’événements peut être contrôlé individuellement, ce qui permet de spécifier des terminaux distincts pour chaque classe d’événements. Les classes d’événements incluent les lampes, les boutons, les affichages, les sonneries, les hookswitch et les flux de médias.

Par exemple, le flux multimédia d’un appel (vocal, par exemple) peut être envoyé à n’importe quel périphérique de transducteur si le fournisseur de services et le matériel sont capables de le faire. En général, un *transducteur* est le même que celui qui est appelé appareil *hookswitch* dans TAPI, qui a un microphone et un haut-parleur. Les événements de sonnerie du commutateur sur le téléphone peuvent être mappés dans une alerte visuelle sur l’écran de l’ordinateur ou ils peuvent être acheminés vers un appareil téléphonique. Les événements de lampe et les événements d’affichage peuvent être ignorés ou acheminés vers un appareil téléphonique (qui semble se comporter comme un ensemble de téléphones normal). Enfin, l’appui sur un bouton sur un appareil téléphonique peut ou non être passé à la ligne. Dans tous les cas, ce routage de signaux de bas niveau à partir de la ligne n’affecte pas le fonctionnement de la partie ligne de l’interface TAPI, qui mappe toujours les événements de bas niveau à leur équivalent fonctionnel. Pour déterminer les terminaux disponibles sur un appareil de ligne (et leurs fonctionnalités), consultez les fonctionnalités de l’appareil en ligne avec [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps).

Supposons à l’origine que l’application a supprimé le routage de tous les événements (avec [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)) et que l’utilisateur sélectionne un casque comme périphérique d’e/s actuel. Un appel entrant envoie un [**message \_ CALLSTATE de ligne**](line-callstate.md) et un message de [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) avec l’indication de la *sonnerie* . Étant donné que le routage de tous les événements est supprimé, les événements Ring ne sont pas routés vers le téléphone, donc la sonnerie est supprimée. Au lieu de cela, l’application avertit l’utilisateur qu’une boîte de dialogue contextuelle et un bip système s’affichent dans le casque.

L’utilisateur décide de répondre à l’appel. Étant donné que le périphérique d’e/s actuel de l’utilisateur est le casque, l’application de téléphonie appelle [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) sur l’appel entrant pour acheminer le média de l’appel au casque et répondre à l’appel. L’application peut également appeler **lineSetTerminal** pour acheminer la lampe et afficher des événements d’informations sur l’ensemble de téléphones pour qu’elle se comporte comme d’habitude.

À titre d’exemple, supposons qu’un appel entrant est une alerte sur l’ordinateur de l’utilisateur. Au lieu de sélectionner l’option de réponse avec la souris, l’utilisateur décide de simplement sélectionner le téléphone du téléphone pour répondre à l’appel. L’État offhook sur le téléphone envoie un message à l’application. L’application peut interpréter cet État comme une demande de la manière dont l’utilisateur sélectionne le téléphone pour effectuer la conversation. L’application appelle ensuite [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) pour acheminer les données de la voix sur l’appel vers l’ensemble téléphonique.

 

 



