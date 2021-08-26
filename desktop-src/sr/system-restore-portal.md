---
title: Restauration du système
description: Définit des points de restauration système et surveille les modifications système principales d’un programme pour permettre une restauration du système à un état antérieur. Écrire du code de récupération automatique ou un script WMI pour restaurer l’état du système sur un point de restauration enregistré.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restauration du système
- Restauration du système, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4472806aa2c0b6f8a29cc4e687d16e262639a66c65bda37fdca970c6c38b656f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111289"
---
# <a name="system-restore"></a>Restauration du système

## <a name="purpose"></a>Objectif

La restauration du système surveille et enregistre automatiquement les modifications système principales sur l’ordinateur d’un utilisateur. Il est conçu pour réduire les coûts de support et accroître la satisfaction des clients en permettant à un utilisateur d’annuler une modification susceptible d’être à l’origine d’un problème au niveau du système, ou de revenir à un jour lorsque le système était optimal.

> [!Note]  
> La documentation suivante est destinée aux développeurs. Si vous êtes un utilisateur final à la recherche d’informations sur l’utilisation de la restauration du système, consultez [qu’est-ce que la restauration du système ?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Développeurs concernés

L’API de restauration du système est conçue pour être utilisée par les programmeurs C/C++. une bonne connaissance de Windows Management Instrumentation (WMI) est nécessaire pour utiliser l’interface de script.

## <a name="run-time-requirements"></a>Conditions d’exécution

l’API de restauration du système est prise en charge sur les systèmes d’exploitation clients à partir de Windows XP. Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser un élément d’API particulier, consultez la section Configuration requise de sa documentation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                | Description                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Vue d'ensemble](about-system-restore.md)<br/>      | Vue d’ensemble du fonctionnement de la restauration du système.<br/>                            |
| [Référence](system-restore-reference.md)<br/> | Documentation des fonctions, structures et classes de restauration du système.<br/> |
| [Exemples](using-system-restore.md)<br/>       | Exemple de programme écrit en C.<br/>                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

