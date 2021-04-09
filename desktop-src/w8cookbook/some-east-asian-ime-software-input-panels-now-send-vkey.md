---
title: Certains panneaux de saisie de logiciel IME pour l’Asie de l’est envoient désormais vKey
description: Certains panneaux de saisie de logiciel IME pour l’Asie de l’est envoient désormais vKey
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840897"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a>Certains panneaux de saisie de logiciel IME pour l’Asie de l’est envoient désormais vKey

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
Serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Dans Windows 8, si l’un des IME asiatiques est sélectionné, le fait d’appuyer sur une touche du panneau de saisie du logiciel n’a pas envoyé vKeys.

Dans Windows 8.1, vKeys sont envoyés pour les configurations suivantes :



| Language            | IME                                 | Windows Store | Bureau |
|---------------------|-------------------------------------|---------------|---------|
| Chinois simplifié  | Microsoft Pinyin, Microsoft Wubi    | Oui           | Oui     |
| Chinois traditionnel | Microsoft Changlie, Microsoft Quick | Oui           | Oui     |
| Chinois traditionnel | Microsoft bopomofo                  | Non            | Non      |
| Coréen              | IME Microsoft                       | Oui           | Non      |
| Japonais            | IME Microsoft                       | Non            | Non      |



 

## <a name="manifestations"></a>Manifestations

Si l’utilisateur choisit un IME qui n’envoie pas de vKeys, les fonctions déclenchées par vKey ne fonctionnent pas.

## <a name="solution"></a>Solution

Les applications qui n’utilisent pas l’une des configurations IME ci-dessus doivent être conçues pour que les utilisateurs puissent terminer la tâche souhaitée sans utiliser de fonctions qui nécessitent vKeys.

Si l’utilisateur choisit un IME qui envoie vKeys, mais que l’application a été conçue sans cette attente, l’application doit être modifiée pour reconnaître la version de Windows en cours d’exécution et répondre en conséquence.

 

 




