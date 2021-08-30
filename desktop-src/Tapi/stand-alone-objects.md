---
description: TAPI 3 implique un certain nombre d’objets qui sont indépendants de ses cinq objets TAPI principaux (TAPI, Address, Call, CallHub et terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Objets Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0094f4409fc6f2ec52d505e29a2f09a2bcff872b159fbd3fafdf7c4ec56f8861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991769"
---
# <a name="stand-alone-objects"></a>Objets Stand-Alone

TAPI 3 implique un certain nombre d’objets qui sont indépendants de ses cinq objets TAPI principaux (TAPI, Address, Call, CallHub et terminal). Les interfaces d' [événements](./event-interfaces.md) et les [interfaces d’énumérateur](enumerator-interfaces.md) sont des objets autonomes et sont résumées séparément. Les éléments suivants résument les interfaces autonomes non-événementielles et non-Enumerator.



| Interface                                             | Description                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | fournit des méthodes pour permettre aux applications clientes Automation telles que Visual Basic de récupérer des informations de collecte.                                                                                             |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | Étend [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) en fournissant des méthodes supplémentaires pour la modification des collections.                                                                                                       |
| [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | Interface COM standard pour l’implémentation de l’automatisation.                                                                                                                                                           |
| [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | Interface COM standard pour l’obtention de pointeurs vers des interfaces d’objet.                                                                                                                                             |
| [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | Permet à une application de récupérer le pointeur de dispatch d’une autre interface sur un objet, en fonction d’un pointeur [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) en cours. Utile pour certains langages de script. |
| [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | Fournit des méthodes qui permettent à une application TAPI 3 d’utiliser la [téléphonie assistée](assisted-telephony-overview.md).                                                                                                |



 



| Interface                                  | Description                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | Démarre, arrête et interrompt les actions en cours, telles qu’une lecture.                                                                                                             |
| [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | Fournit des méthodes spécifiques à la lecture qui permettent à une application d’effectuer des opérations telles que définir la liste des fichiers à lire et modifier la vitesse de lecture.              |
| [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | Fournit des méthodes spécifiques à l’enregistrement qui permettent à une application d’effectuer des opérations telles que la définition des noms des fichiers à enregistrer et la modification de la durée d’un enregistrement. |



 



| Interface                                                  | Description                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITScriptableAudioFormat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | Récupère le format audio de ou définit le format audio pour une piste.                                                                                             |
| [**ITStaticAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | Fournit des méthodes sur les objets de terminal audio statiques qui sont nécessaires pour prendre en charge les appareils téléphoniques. Les MSP TAPI 3,1 doivent exposer cette interface sur tous les terminaux audio statiques. |



 

 

 
