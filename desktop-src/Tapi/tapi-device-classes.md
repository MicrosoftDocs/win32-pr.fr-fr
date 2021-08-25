---
description: En savoir plus sur les classes de périphériques TAPI. Une classe d’appareils est un groupe d’appareils ou de pilotes de périphérique par le biais duquel les applications envoient et reçoivent des informations ou des données d’appel.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: Classes d’appareils TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f277e74012241139cf619c5229c4525711d93304f7321809461aff13416e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975479"
---
# <a name="tapi-device-classes"></a>Classes d’appareils TAPI

Une classe d’appareils est un groupe de périphériques physiques ou de pilotes de périphérique associés par le biais desquels les applications envoient et reçoivent les informations ou les données qui constituent un appel. Chaque classe d’appareil a un *nom de classe d’appareil* qui identifie de façon unique la classe, et fournit des informations sur l’interface de programmation et les commandes qui peuvent être utilisées pour ouvrir et communiquer avec les appareils de la classe.

L’interface de programmation d’applications de téléphonie (TAPI) associe des appareils d’une ou plusieurs classes d’appareils à chaque périphérique téléphonique ou ligne. Pour accéder à l’un de ces appareils, récupérez l’identificateur de l’appareil pour l’appareil à l’aide de la fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) ou [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) . Vous fournissez le nom de classe de l’appareil et la fonction retourne le nom de port, le nom de périphérique, le descripteur d’appareil ou l’identificateur de périphérique spécifique que vous devez ouvrir et accéder à l’appareil. Le format des informations retournées dépend de la classe de l’appareil et est décrit dans les rubriques suivantes de cette section.

Vous utilisez également des noms de classes d’appareils avec les fonctions [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) et [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) pour permettre à l’utilisateur de définir des options de configuration pour l’appareil donné, avec les fonctions [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) et [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) pour récupérer une icône représentant l’appareil donné, et avec les fonctions [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) et [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) pour récupérer et définir directement les options de configuration pour le périphérique donné.

La liste suivante répertorie les noms de classes d’appareils.



| Nom de classe de l’appareil                                      | Description                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [comm](comm.md)                                       | Port de communication.                              |
| [comm/datamodem](comm-datamodem.md)                   | Modem via un port de communication.              |
| [comm/datamodem/PortName](comm-datamodem-portname.md) | Nom de l’appareil auquel un modem est connecté. |
| [Wave/entrée](wave-in.md)                                 | Périphérique Wave Audio (entrée uniquement).                   |
| [Wave/sortie](wave-out.md)                               | Périphérique Wave Audio (sortie uniquement).                  |
| [Wave/entrée/sortie](wave-in-out.md)                         | Périphérique audio Wave, Full duplex.                   |
| [midi/in](midi-in.md)                                 | Séquenceur MIDI (entrée uniquement).                      |
| [midi/out](midi-out.md)                               | Séquenceur MIDI (sortie uniquement).                     |
| [TAPI/ligne](tapi-line.md)                             | Périphérique de ligne.                                      |
| [TAPI/téléphone](tapi-phone.md)                           | Téléphone appareil.                                     |
| [NDIS](ndis.md)                                       | Périphérique réseau.                                   |
| [TAPI/terminal](tapi-terminal.md)                     | Appareil Terminal Server.                                  |



 

> [!Note]  
> Ces noms ne respectent pas la casse ; vous pouvez utiliser n’importe quelle combinaison de lettres majuscules et minuscules.

 

Des classes d’appareils et des noms de classes d’appareils supplémentaires peuvent être disponibles sur un système donné. En général, si un appareil n’appartient pas à l’une des classes de périphérique par défaut, le fabricant définit généralement une nouvelle classe de périphérique et attribue un nom de classe d’appareil unique. Consultez la documentation de l’appareil pour déterminer les classes d’appareils supplémentaires disponibles pour celui-ci. Notez, cependant, que même si la classe d’appareil et le type de média sont associés, ils ne sont pas identiques. Un type de média décrit le format des informations sur les appels, et une classe d’appareil définit l’interface de programmation utilisée pour gérer ces informations. Ainsi, même si un fabricant définit un nouveau type de média, il n’est pas nécessairement vrai que le fabricant doive également définir une nouvelle classe d’appareil pour prendre en charge le mode.

Le format des données de configuration utilisées avec les fonctions [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) et [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) dépend également de la classe de l’appareil. En général, vous utilisez **lineGetDevConfig** pour enregistrer une copie des données de configuration d’appareil actuelles, puis vous utilisez ensuite **lineSetDevConfig** avec les données de configuration enregistrées pour restaurer la configuration de l’appareil à l’état précédent. Il s’agit d’un moyen pratique de modifier temporairement la configuration sans demander à l’utilisateur de la restaurer manuellement à l’état précédent. Étant donné que le format exact des données de configuration de l’appareil peut être différent avec chaque fournisseur de services, vous ne devez pas utiliser **lineSetDevConfig** et **lineGetDevConfig** pour manipuler directement les données de configuration de l’appareil. Certains formats sont fournis uniquement pour les informations.

 

 



