---
title: Modifications du modèle en mode IME
description: Modèle mode IME remplacé par utilisateur par thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443245"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Modèle mode IME remplacé par utilisateur par thread

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
Serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Dans Windows 8, le mode de conversion IME et le mode phrase IME étaient basés sur le contexte de l’utilisateur, et la modification du mode d’une application a affecté toutes les autres applications. Ce comportement peut être désactivé à l’aide de la paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » dans la section Paramètres avancés du panneau de configuration de langue.

Pour améliorer la compatibilité, dans Windows 8.1 les modes sont stockés dans un contexte d’entrée, quelle que soit la façon dont le contrôle « me laisser définir une méthode d’entrée différente pour chaque fenêtre d’application » est défini. Dans Windows 8.1, le paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » affecte uniquement la sélection de la méthode d’entrée proprement dite.

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

 

 