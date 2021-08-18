---
description: sécurité (Windows 7 et Windows Server 2008 R2-guide de qualité des applications)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: sécurité (Windows 7 et Windows Server 2008 R2-guide de qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d392f5bf14997962173b9054baba861003877d851d6bd62a947b15757feec23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994659"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>sécurité (Windows 7 et Windows Server 2008 R2-guide de qualité des applications)

à compter de Windows internet explorer 7, Windows internet explorer s’exécute dans un contexte de sécurité appelé *Mode protégé* quand les utilisateurs l’exécutent sur le système d’exploitation Windows Vista ou une version ultérieure. ce mode exécute Internet Explorer dans un paramètre de privilège inférieur à celui d’une application utilisateur standard, de sorte que certaines fonctionnalités sont limitées, en particulier ActiveX contrôles et certains types de plug-ins. Pour plus d’informations sur le mode protégé dans Internet Explorer et son impact sur la compatibilité, consultez [présentation et utilisation en mode protégé d’Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) dans la bibliothèque MSDN.

par défaut, Windows Internet Explorer 8 active également la prévention de l’exécution des données (DEP), qui permet aux applications d’éviter d’exécuter du code arbitraire dans les attaques en ligne. toutefois, certains modules complémentaires peuvent ne pas utiliser cette fonctionnalité de sécurité (par exemple, tous les modules complémentaires qui ne sont pas conçus pour exécuter uniquement le code qui se trouve dans la mémoire qui a été spécifiquement marquée comme exécutable, comme les applications générées à l’aide d’une version antérieure de l’infrastructure ActiveX Template Library (ATL)).

Internet Explorer 8 protège également les utilisateurs contre les failles de sécurité potentielles qui utilisent des scripts. Par exemple, vous ne pouvez pas naviguer d’une URL dans une zone moins fiable vers une URL dans une zone plus fiable, sauf via une interaction utilisateur explicite. Vous ne pouvez pas non plus masquer certains éléments de l’interface utilisateur du navigateur (tels que la barre d’adresses) dans une zone non approuvée (Internet).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
