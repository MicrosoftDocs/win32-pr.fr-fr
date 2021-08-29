---
title: Modifications du modèle en mode IME
description: Modèle mode IME remplacé par utilisateur par thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c86c8ba5e00bf4fb47d2908e626736252a8a6dc54b9c6ac4fa866782fde8d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815199"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Modèle mode IME remplacé par utilisateur par thread

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

dans Windows 8, le mode de Conversion ime et le mode phrase ime étaient basés sur le contexte utilisateur, et la modification du mode d’une application a affecté toutes les autres applications. Ce comportement peut être désactivé à l’aide de la paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » dans la section Paramètres avancés du panneau de configuration de langue.

pour améliorer la compatibilité, dans Windows 8.1 les modes sont stockés dans un contexte d’entrée, quelle que soit la façon dont le contrôle « me laisser définir une méthode d’entrée différente pour chaque fenêtre d’application » est défini. dans Windows 8.1, le paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » affecte uniquement la sélection de la méthode d’entrée proprement dite.

Au démarrage de l’application, le mode IME est défini sur les valeurs par défaut suivantes :



| &nbsp;   | Panneau de saisie du logiciel | Clavier matériel |
|----------|----------------------|-------------------|
| KOR, JPN | Activé                   | Désactivé               |
| CHS, CHT  | Activé                   | Activé                |



 

## <a name="manifestations"></a>Manifestations

Quand un utilisateur modifie le mode IME sur une application, la modification n’affecte pas les autres applications.

## <a name="resources"></a>Ressources

-   [Valeurs du mode de conversion IME](../intl/ime-conversion-mode-values.md)
-   [Valeurs du mode de phrase IME](../intl/ime-sentence-mode-values.md)

 

 