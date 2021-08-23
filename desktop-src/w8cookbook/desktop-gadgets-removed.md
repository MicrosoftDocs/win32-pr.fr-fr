---
title: Gadgets du Bureau supprimés
description: Gadgets du Bureau supprimés
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Gadgets
- gadgets du Bureau
- Windows Encadré
- Barre latérale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254c4794c93c6afeeec9374e7c1c73f7d538c82b343ffaea984369a72231deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707009"
---
# <a name="desktop-gadgets-removed"></a>Gadgets du Bureau supprimés

## <a name="platforms"></a>Plateformes

 **Clients** -Windows 8  
**serveurs** -Windows Server 2012  



## <a name="description"></a>Description

Du point de vue des fonctionnalités, les gadgets ont déjà été dépréciés et sont déclassés par de nouvelles vignettes et applications dynamiques. Les gadgets présentent également un risque pour la sécurité pour les utilisateurs. En tant que plateforme, il existe des vulnérabilités telles que des gadgets sans gravité pourraient être exploités. par conséquent, pour respecter Windows 8 comme système d’exploitation le plus moderne et le plus sécurisé, nous avons choisi de supprimer entièrement les Gadgets du système d’exploitation. Windows 7 les utilisateurs avec des gadgets sur leur bureau seront avertis et les gadgets seront désinstallés.

## <a name="manifestation"></a>Manifestation

les Gadgets du bureau ne sont pas disponibles sur le bureau de Windows.

## <a name="mitigation"></a>Limitation des risques

L’API et la structure de dossiers des gadgets Desktop restent en place pour Windows 8. Les applications qui installent et exécutent par programme des gadgets à l’aide de cette API continuent de s’exécuter sans échec (même si les gadgets eux-mêmes ne le sont pas).

## <a name="solution"></a>Solution

Les développeurs d’applications de bureau ne doivent pas empaqueter des gadgets dans leurs programmes d’installation. Ces gadgets occupent simplement de l’espace pour l’utilisateur et ne peuvent pas être exécutés dans le système.

## <a name="tests"></a>Tests

les développeurs sont en mesure de tester la compatibilité de ce changement en désactivant le composant facultatif pour les Gadgets de bureau dans Windows 7. pour désactiver les Gadgets sur un PC Windows 7, procédez comme suit :

1.  accédez à activer ou désactiver des fonctionnalités Windows dans le panneau de configuration.
2.  désactivez la case à cocher en regard de « Windows Gadget Platform ».
3.  Cliquez sur OK et suivez les autres instructions à l’écran.

## <a name="resources"></a>Ressources

[Des vulnérabilités dans les gadgets pourraient permettre l’exécution de code à distance](https://support.microsoft.com/kb/2719662)

 

 




