---
title: Gadgets du Bureau supprimés
description: Gadgets du Bureau supprimés
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Gadgets
- gadgets du Bureau
- Encadré Windows
- Barre latérale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104383040"
---
# <a name="desktop-gadgets-removed"></a>Gadgets du Bureau supprimés

## <a name="platforms"></a>Plateformes

 **Clients** -Windows 8  
**Serveurs** -Windows Server 2012  



## <a name="description"></a>Description

Du point de vue des fonctionnalités, les gadgets ont déjà été dépréciés et sont déclassés par de nouvelles vignettes et applications dynamiques. Les gadgets présentent également un risque pour la sécurité pour les utilisateurs. En tant que plateforme, il existe des vulnérabilités telles que des gadgets sans gravité pourraient être exploités. Par conséquent, afin de respecter Windows 8 comme système d’exploitation le plus moderne et le plus sécurisé, nous avons choisi de supprimer entièrement les gadgets du système d’exploitation. Les utilisateurs de Windows 7 avec des gadgets sur leur bureau seront avertis et les gadgets seront désinstallés.

## <a name="manifestation"></a>Manifestation

Les gadgets du Bureau ne sont pas disponibles sur le bureau Windows.

## <a name="mitigation"></a>Limitation des risques

L’API et la structure des dossiers des gadgets Desktop resteront en place pour Windows 8. Les applications qui installent et exécutent par programme des gadgets à l’aide de cette API continuent de s’exécuter sans échec (même si les gadgets eux-mêmes ne le sont pas).

## <a name="solution"></a>Solution

Les développeurs d’applications de bureau ne doivent pas empaqueter des gadgets dans leurs programmes d’installation. Ces gadgets occupent simplement de l’espace pour l’utilisateur et ne peuvent pas être exécutés dans le système.

## <a name="tests"></a>Tests

Les développeurs sont en mesure de tester la compatibilité de ce changement en désactivant le composant facultatif pour les gadgets de bureau dans Windows 7. Pour désactiver les gadgets sur un PC Windows 7, procédez comme suit :

1.  Accédez à activer ou désactiver des fonctionnalités Windows dans le panneau de configuration.
2.  Désactivez la case à cocher en regard de « plateforme Gadget Windows ».
3.  Cliquez sur OK et suivez les autres instructions à l’écran.

## <a name="resources"></a>Ressources

[Des vulnérabilités dans les gadgets pourraient permettre l’exécution de code à distance](https://support.microsoft.com/kb/2719662)

 

 




