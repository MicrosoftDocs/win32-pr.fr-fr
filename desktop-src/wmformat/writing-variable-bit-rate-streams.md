---
title: Écriture de flux de vitesse binaire variable
description: Écriture de flux de vitesse binaire variable
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- ASF (Advanced Systems Format), écriture de flux VBR
- ASF (Advanced Systems Format), écriture de flux VBR
- Vitesse de transmission variable (VBR), écriture de flux
- VBR (vitesse de transmission variable), écriture de flux
- flux, écriture VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723394"
---
# <a name="writing-variable-bit-rate-streams"></a>Écriture de flux de vitesse binaire variable

Les flux à débit binaire variable (VBR) sont écrits de la même façon que les flux à débit binaire constant (CBR). La seule différence réside dans le traitement effectué en interne par le writer et les codecs. Toutefois, le VBR basé sur la vitesse binaire (à la fois contraint et sans contrainte) requiert une passe de prétraitement dans le writer.

Vous devez vérifier la valeur de retour pour le premier appel que vous apportez à [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) pour chaque flux. Si le code d’erreur retourné est NS \_ E \_ nombre de passes non valides \_ \_ , le flux requiert une passe de prétraitement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de l’encodage Two-Pass**](using-two-pass-encoding.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




