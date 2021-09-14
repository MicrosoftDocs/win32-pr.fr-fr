---
description: Un administrateur peut utiliser les méthodes suivantes pour permettre à un utilisateur non-administrateur d’installer une application avec des privilèges système élevés.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Installation d’un package avec des privilèges élevés pour un non-administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81de333d6ca388017e03c96f739d7bd258a7c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012057"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Installation d’un package avec des privilèges élevés pour un non-administrateur

Un administrateur peut utiliser les méthodes suivantes pour permettre à un utilisateur non-administrateur d’installer une application avec des privilèges système élevés.

-   dans Windows Vista avec Windows Installer, un membre du groupe administrateurs peut accorder l’autorisation à un non-administrateur d’élever l’installation par le biais du [*contrôle de compte d’utilisateur*](u-gly.md) (uac), comme décrit dans utilisation de [Windows Installer avec uac](using-windows-installer-with-uac.md).

    **Windows Vista :** Obligatoire.

Les méthodes suivantes peuvent également être utilisées pour installer une application avec des privilèges système élevés.

-   un administrateur peut publier une application sur l’ordinateur d’un utilisateur en affectant ou en publiant le package Windows Installer à l’aide du déploiement d’applications et de [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page). L’administrateur publie le package pour l’installation par ordinateur. Si un utilisateur qui n’est pas administrateur installe ensuite l’application, l’installation peut s’exécuter avec des privilèges élevés. Les utilisateurs non-administrateurs ne peuvent pas installer les packages non publiés qui nécessitent des privilèges système élevés.
-   Un administrateur peut accéder à l’ordinateur de l’utilisateur et [publier](advertisement.md) l’application pour une installation par ordinateur. étant donné que le Windows Installer a toujours des privilèges élevés lors de l’installation dans le [contexte d’installation](installation-context.md)par ordinateur, si un utilisateur non-administrateur installe ensuite l’application publiée, l’installation peut s’exécuter avec des privilèges élevés. Les utilisateurs non-administrateurs ne peuvent toujours pas installer les packages non publiés qui requièrent des privilèges élevés.
-   Un utilisateur sans privilèges peut installer une application publiée qui requiert des privilèges élevés si un agent du système local publie l’application. L’application peut être publiée pour une installation par utilisateur ou par ordinateur. Une application installée à l’aide de cette méthode est considérée comme gérée. Pour plus d’informations, consultez [publication d’une Application Per-User à installer avec des privilèges élevés](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Un administrateur peut définir la stratégie [AlwaysInstallElevated a](alwaysinstallelevated.md) pour les installations par utilisateur et par ordinateur. Cette méthode peut ouvrir un ordinateur à un risque de sécurité, car lorsque cette stratégie est définie, un utilisateur non-administrateur peut exécuter des installations avec des privilèges élevés et accéder à des emplacements sécurisés sur l’ordinateur, tels que SystemFolder ou la clé de Registre **HKLM** .

    Si l’application est installée par ordinateur pendant que la stratégie [AlwaysInstallElevated a](alwaysinstallelevated.md) est définie, le produit est traité comme géré. Dans ce cas, l’application peut toujours effectuer une réparation avec des privilèges élevés si la stratégie est supprimée. En outre, si l’application est installée par utilisateur pendant que la stratégie AlwaysInstallElevated a est définie, l’application ne peut pas effectuer de réparation si la stratégie est supprimée.

-   Un administrateur peut accéder à l’ordinateur d’un utilisateur et effectuer une installation par ordinateur de l’application. Étant donné que les privilèges sont requis pour effectuer ce type d’installation, les installations par ordinateur sont toujours gérées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contexte d’installation](installation-context.md)
</dt> </dl>

 

 
