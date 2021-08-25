---
description: Un seul téléphone peut être en mesure d’sonner avec différents modes de sonnerie.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anneau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d183c217447ca02bf5ee0c535360eecaea1f3c209cdb813ad58b77268f234d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773359"
---
# <a name="ring"></a>Anneau

Un seul téléphone peut être en mesure d’sonner avec différents modes de sonnerie. Étant donné la grande variété de modes de sonnerie disponibles, les modes Ring sont identifiés par le biais de leur numéro en mode Ring. Un nombre en mode Ring est compris entre zéro et le nombre de modes Ring disponibles moins un.

Les fonctions qu’une application utiliserait pour contrôler les modes ring d’un appareil téléphonique sont [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), qui sonne un appareil téléphonique ouvert en fonction d’un mode Ring donné et [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), qui retourne le mode Ring actuel d’un appareil téléphonique ouvert.

Lorsque le mode ring d’un appareil téléphonique est modifié, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à l’application pour notifier l’application du changement d’État. Les paramètres de ce message fournissent une indication de la modification.

 

 



