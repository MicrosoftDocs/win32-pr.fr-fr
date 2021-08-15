---
description: Sous-ensemble de .NET 2,0 maintenant sur Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Sous-ensemble de .NET 2,0 maintenant sur Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9da259186f0eaea7999df6dde6d42d972484c35eee24c9b9efb7fc6a5d882b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994629"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Sous-ensemble de .NET 2,0 maintenant sur Server Core

## <a name="platform"></a>Plateforme

**serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

l’option d’installation server Core pour Windows server 2008 R2 comprend désormais un sous-ensemble des .NET Framework 2,0. Le sous-ensemble est la fonctionnalité de .NET 2,0 qui s’aligne sur les fonctionnalités de Server Core. aucun binaire n’a été ajouté à la base Server Core pour permettre à n’importe quelle partie de .NET 2,0 de fonctionner.

l’option d’installation server Core n’a pas été prise en charge par .net pour Windows server 2008.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

cela permet à certaines applications basées sur .net 2,0 de s’exécuter sur server Core dans Windows server 2008 R2.

## <a name="testing"></a>Test

Vérifiez que les classes .NET utilisées par votre code sont incluses dans Server Core. Testez également toutes les applications qui exécutent ce code sur Server Core.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Blog Server Core](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *voir aussi* la section Server Core du *kit de développement logiciel (SDK) Windows server 2008 R2* dès qu’elle sera disponible

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.

 

 

 
