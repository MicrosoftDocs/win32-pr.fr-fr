---
title: Écriture d’une vitesse de transmission variable Flux
description: Écriture d’une vitesse de transmission variable Flux
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- ASF (Advanced Systems Format), écriture de flux VBR
- ASF (Advanced Systems Format), écriture de flux VBR
- Vitesse de transmission variable (VBR), écriture de flux
- VBR (vitesse de transmission variable), écriture de flux
- flux, écriture VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694774613ada8b4be05eab55be3213898d423d3b6ac4438204d149a0bd606c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930255"
---
# <a name="writing-variable-bit-rate-streams"></a>Écriture d’une vitesse de transmission variable Flux

Les flux à débit binaire variable (VBR) sont écrits de la même façon que les flux à débit binaire constant (CBR). La seule différence réside dans le traitement effectué en interne par le writer et les codecs. Toutefois, le VBR basé sur la vitesse binaire (à la fois contraint et sans contrainte) requiert une passe de prétraitement dans le writer.

Vous devez vérifier la valeur de retour pour le premier appel que vous apportez à [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) pour chaque flux. Si le code d’erreur retourné est NS \_ E \_ nombre de passes non valides \_ \_ , le flux requiert une passe de prétraitement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de l’encodage Two-Pass**](using-two-pass-encoding.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




