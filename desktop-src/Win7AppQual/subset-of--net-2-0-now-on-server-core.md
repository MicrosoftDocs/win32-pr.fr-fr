---
description: Sous-ensemble de .NET 2,0 maintenant sur Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Sous-ensemble de .NET 2,0 maintenant sur Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6ef839f525acf190df384e3fe8394f2b785d45
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116147"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Sous-ensemble de .NET 2,0 maintenant sur Server Core

## <a name="platform"></a>Plateforme

**Serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

L’option d’installation Server Core pour Windows Server 2008 R2 comprend désormais un sous-ensemble des .NET Framework 2,0. Le sous-ensemble est la fonctionnalité de .NET 2,0 qui s’aligne sur les fonctionnalités de Server Core. aucun binaire n’a été ajouté à la base Server Core pour permettre à n’importe quelle partie de .NET 2,0 de fonctionner.

Il n’existait aucune prise en charge .NET dans l’option d’installation Server Core pour Windows Server 2008.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Cela permet à certaines applications basées sur .NET 2,0 de s’exécuter sur Server Core dans Windows Server 2008 R2.

## <a name="testing"></a>Test

Vérifiez que les classes .NET utilisées par votre code sont incluses dans Server Core. Testez également toutes les applications qui exécutent ce code sur Server Core.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Blog Server Core](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Voir aussi* la section Server Core du *Kit de développement logiciel (SDK) Windows Server 2008 R2* quand elle est disponible

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.

 

 

 
