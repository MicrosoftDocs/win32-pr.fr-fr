---
description: En savoir plus sur les classes d’appareils TSPI. Une classe d’appareils est un groupe d’appareils ou de pilotes de périphérique par le biais duquel les applications envoient et reçoivent des informations ou des données d’appel.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: Classes d’appareils TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6775e73df3914339edbdf791659de821855864dd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011342"
---
# <a name="tspi-device-classes"></a>Classes d’appareils TSPI

Une *classe d’appareils* est un groupe de périphériques physiques ou de pilotes de périphérique associés par le biais desquels les applications envoient et reçoivent les informations ou les données qui constituent un appel. Chaque classe d’appareil a un *nom de classe d’appareil* qui identifie de façon unique la classe et fournit des informations sur l’interface de programmation et les commandes qui peuvent être utilisées pour ouvrir et communiquer avec les appareils de la classe.

L’interface de programmation d’applications de téléphonie (TAPI) associe des appareils d’une ou plusieurs classes d’appareils à chaque périphérique téléphonique ou ligne. Pour accéder à l’un de ces appareils, récupérez l’identificateur de l’appareil pour l’appareil à l’aide de la fonction [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) ou [**phoneGetID**](/windows/win32/api/tapi/nf-tapi-phonegetid) . Vous fournissez le nom de classe de l’appareil et la fonction retourne le nom de port, le nom de périphérique, le descripteur d’appareil ou l’identificateur de périphérique spécifique que vous devez ouvrir et accéder à l’appareil. Le format des informations retournées dépend de la classe de l’appareil et est décrit dans cette section.

Vous utilisez également des noms de classes d’appareils avec les fonctions [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) et [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) pour permettre à l’utilisateur de définir des options de configuration pour l’appareil donné. avec les fonctions [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) et [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) pour récupérer une icône représentant l’appareil donné ; et avec les fonctions [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) et [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) pour récupérer et définir directement les options de configuration pour l’appareil donné.

Voici les noms de classes d’appareil par défaut.



| Nom de classe de l’appareil                                       | Description                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [comm](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Port de communication                              |
| [comm/datamodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem via un port de communication              |
| [comm/datamodem/PortName](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Nom de l’appareil auquel un modem est connecté |
| [Wave/entrée](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Périphérique Wave Audio (entrée uniquement)                   |
| [Wave/sortie](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Périphérique Wave Audio (sortie uniquement)                  |
| [Wave/entrée/sortie](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Périphérique audio Wave, Full duplex                   |
| [midi/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | Séquenceur MIDI (entrée uniquement)                      |
| [midi/out](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | Séquenceur MIDI (sortie uniquement)                     |
| [TAPI/ligne](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Périphérique de ligne                                      |
| [TAPI/téléphone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Appareil téléphonique                                     |
| [NDIS](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Appareil réseau                                   |
| [TAPI/terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Appareil terminal                                  |



 

Ces noms ne respectant pas la casse, vous pouvez utiliser n’importe quelle combinaison de lettres majuscules et minuscules.

Des classes d’appareils et des noms de classes d’appareils supplémentaires peuvent être disponibles sur un système donné. En général, si un appareil n’appartient pas à l’une des classes de périphérique par défaut, le fabricant définit généralement une nouvelle classe de périphérique et attribue un nom de classe d’appareil unique. Vous devez vérifier la documentation de l’appareil pour déterminer quelles classes d’appareils supplémentaires sont disponibles pour celui-ci. Notez, cependant, que même si la classe d’appareil et le type de média sont associés, ils ne sont pas identiques. Un *type de média* décrit un format d’informations sur un appel, et une *classe d’appareil* définit l’interface de programmation utilisée pour gérer ces informations. Ainsi, même si un fabricant définit un nouveau type de média, il peut ne pas être vrai que le fabricant doit également définir une nouvelle classe d’appareil pour prendre en charge le mode.

Le format des données de configuration utilisées avec les fonctions [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) et [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) dépend également de la classe de l’appareil. En général, vous utilisez **lineGetDevConfig** pour enregistrer une copie des données de configuration d’appareil actuelles, puis vous utilisez ensuite **lineSetDevConfig** avec les données de configuration enregistrées pour restaurer la configuration de l’appareil à l’état précédent. Il s’agit d’un moyen pratique de modifier temporairement la configuration sans demander à l’utilisateur de la restaurer manuellement à l’état précédent. Étant donné que le format exact des données de configuration de l’appareil peut être différent avec chaque fournisseur de services, n’utilisez pas **lineSetDevConfig** et **lineGetDevConfig** pour manipuler les données de configuration de l’appareil directement. Certains formats sont fournis à titre d’information uniquement.

 

 
