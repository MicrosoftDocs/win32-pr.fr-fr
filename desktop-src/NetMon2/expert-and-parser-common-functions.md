---
description: Les fonctions Moniteur réseau, énumérées dans le tableau suivant, peuvent être utilisées pour développer des analyseurs ou des experts.
ms.assetid: 26eb4f99-a8dc-43a2-abb9-9577518b6f2f
title: Fonctions courantes des experts et de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6776260610c2decb0ecf91b6373d301937d899b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229637"
---
# <a name="expert-and-parser-common-functions"></a>Fonctions courantes des experts et de l’analyseur

Les fonctions Moniteur réseau, énumérées dans le tableau suivant, peuvent être utilisées pour développer des [*analyseurs*](p.md) ou des [*experts*](e.md).



| Fonction                                                               | Description                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [CompareAddresses](compareaddresses.md)                               | Compare deux adresses données.                                                       |
| [CompareFrameDestAddress](compareframedestaddress.md)                 | Compare une adresse donnée à l’adresse de destination d’un frame.                     |
| [CompareFrameSourceAddress](compareframesourceaddress.md)             | Compare une adresse donnée à l’adresse source d’un frame.                          |
| [FilterAddObject](filteraddobject.md)                                 | Ajoute un seul objet à un filtre.                                                   |
| [FindPropertyInstance](findpropertyinstance.md)                       | Recherche la première instance d’une propriété donnée.                                       |
| [FindPropertyInstanceRestart](findpropertyinstancerestart.md)         | Recherche l’instance suivante d’une propriété donnée.                                        |
| [GetCaptureComment](getcapturecomment.md)                             | Récupère le commentaire d’une capture.                                                 |
| [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)     | Récupère le commentaire d’une capture à partir de son fichier de capture.                           |
| [GetCaptureMacType](getcapturemactype.md)                             | Récupère le type MAC de la capture.                                              |
| [GetCaptureTimeStamp](getcapturetimestamp.md)                         | Récupère le datage du délai de capture.                                                |
| [GetCaptureTotalFrames](getcapturetotalframes.md)                     | Récupère le nombre total de frames dans la capture.                                          |
| [GetEnabledProtocols](getenabledprotocols.md)                         | Récupère une liste de tous les protocoles marqués comme activés.                            |
| [GetFrame](getframe.md)                                               | Récupère un handle vers un frame donné.                                                |
| [GetFrameCaptureHandle](getframecapturehandle.md)                     | Récupère un handle vers une capture donnée.                                              |
| [GetFrameDstAddressOffset](getframedstaddressoffset.md)               | Récupère le décalage d’adresse de destination pour un frame donné.                         |
| [GetFrameFromFrameHandle](getframefromframehandle.md)                 | Récupère un frame pour un handle de frame donné.                                         |
| [GetFrameLength](getframelength.md)                                   | Récupère la longueur d’un frame donné.                                              |
| [GetFrameMacHeaderLength](getframemacheaderlength.md)                 | Récupère la longueur de l’en-tête MAC pour un frame donné.                           |
| [GetFrameMacType](getframemactype.md)                                 | Récupère le type MAC pour un frame donné.                                           |
| [GetFrameNumber](getframenumber.md)                                   | Retourne le nombre d’un frame donné.                                                |
| [GetFrameRecognizeData](getframerecognizedata.md)                     | Récupère les identificateurs de protocole (et leurs offsets) de tous les protocoles reconnus. |
| [GetFrameSrcAddressOffset](getframesrcaddressoffset.md)               | Récupère le décalage à l’adresse source d’un frame donné.                        |
| [GetFrameStoredLength](getframestoredlength.md)                       | Récupère la longueur d’un frame donné.                                              |
| [GetFrameTimeStamp](getframetimestamp.md)                             | Récupère l’horodatage d’un frame donné.                                          |
| [GetPreviousProtocolOffsetByName](getpreviousprotocoloffsetbyname.md) | Récupère l’instance précédente d’un protocole donné.                                |
| [GetProperty](getproperty.md)                                         | Récupère une propriété avec un nom donné.                                             |
| [GetPropertyInfo](getpropertyinfo.md)                                 | Récupère les informations d’une propriété spécifique.                                   |
| [GetPropertyText](getpropertytext.md)                                 | Récupère le texte d’une propriété donnée.                                             |
| [GetProtocolFromName](getprotocolfromname.md)                         | Récupère un protocole spécifique par nom.                                              |
| [GetProtocolInfo](getprotocolinfo.md)                                 | Utilise le handle de protocole pour récupérer les données relatives aux protocoles.                        |
| [GetProtocolStartOffsetHandle](getprotocolstartoffsethandle.md)       | Récupère le décalage d’un protocole donné.                                           |
| [MacTypeToAddressType](mactypetoaddresstype.md)                       | Convertit un type MAC en type d’adresse.                                             |
| [ModifyFrame](modifyframe.md)                                         | Met à jour un frame existant avec les nouvelles données.                                            |



 

Pour plus d’informations sur les fonctions et les structures uniquement utilisées par les experts, et les fonctions et structures uniquement utilisées par les analyseurs, consultez les rubriques figurant dans le tableau suivant.



| Pour plus d’informations sur l’un des sujets suivants :                                          | Consultez                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Fonctions spécifiques à l’expert que vous pouvez utiliser pour développer des dll d’experts. | [Fonctions, structures et énumérations d’experts](expert-functions-structures-and-enumerations.md) |
| Fonctions spécifiques à l’analyseur que vous pouvez utiliser pour développer des dll d’analyseur. | [Structures et fonctions de l’analyseur](parser-functions-and-structures.md)                             |



 

 

 



