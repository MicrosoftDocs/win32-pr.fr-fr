---
description: L’objet de requête est créé à l’aide de COM CoCreateInstance et expose une interface, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objet Request
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcf6da101c3642ffe31b05efb18279a79bcfc28ed24af7a959f3275d9cbc4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905889"
---
# <a name="request-object"></a>Objet Request

L’objet de requête est créé à l’aide de COM **CoCreateInstance** et expose une interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Cette interface expose la méthode [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , qui permet à une application TAPI 3 d’utiliser la téléphonie assistée. La téléphonie assistée fournit aux applications prenant en charge la téléphonie un mécanisme simple pour effectuer des appels téléphoniques sans que le développeur n’ait besoin d’être entièrement responsable de la téléphonie.

Par exemple, une application de feuille de calcul peut ajouter un bouton « téléphoner » à l’aide de la téléphonie assistée sans implémenter les contrôles plus élaborés disponibles dans une application TAPI complète.

Pour plus d’informations, consultez la [vue d’ensemble de la téléphonie assistée](assisted-telephony-overview.md) .

 

 



