---
description: Sécurité (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sécurité (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116227"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Sécurité (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)

À compter de Windows Internet Explorer 7, Windows Internet Explorer s’exécute dans un contexte de sécurité appelé *mode protégé* quand les utilisateurs l’exécutent sur le système d’exploitation Windows Vista ou une version ultérieure. Ce mode exécute Internet Explorer dans un paramètre de privilège inférieur à celui d’une application utilisateur standard, de sorte que certaines fonctionnalités sont limitées, en particulier les contrôles ActiveX et certains types de plug-ins. Pour plus d’informations sur le mode protégé dans Internet Explorer et son impact sur la compatibilité, consultez [présentation et utilisation en mode protégé d’Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) dans la bibliothèque MSDN.

Par défaut, Windows Internet Explorer 8 active également la prévention de l’exécution des données (DEP), qui permet aux applications d’éviter d’exécuter du code arbitraire dans les attaques en ligne. Toutefois, certains modules complémentaires peuvent ne pas utiliser cette fonctionnalité de sécurité (par exemple, tous les modules complémentaires qui ne sont pas conçus pour exécuter uniquement le code qui se trouve dans la mémoire qui a été spécifiquement marquée comme exécutable, comme les applications générées à l’aide d’une version antérieure de l’infrastructure ATL (ActiveX Template Library)).

Internet Explorer 8 protège également les utilisateurs contre les failles de sécurité potentielles qui utilisent des scripts. Par exemple, vous ne pouvez pas naviguer d’une URL dans une zone moins fiable vers une URL dans une zone plus fiable, sauf via une interaction utilisateur explicite. Vous ne pouvez pas non plus masquer certains éléments de l’interface utilisateur du navigateur (tels que la barre d’adresses) dans une zone non approuvée (Internet).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
