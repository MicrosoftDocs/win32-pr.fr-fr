---
description: .
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Résolution des problèmes de compatibilité de l’installation ActiveX pour les utilisateurs standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e50ed2aa9e428164e39b377b65c418d82df1e5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761437"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Résolution des problèmes de compatibilité de l’installation ActiveX pour les utilisateurs standard

Pour développer un environnement de bureau sécurisé, vous devez atténuer les menaces des contrôles ActiveX malveillants et fournir un niveau approprié de compatibilité des applications dans votre environnement. Un *contrôle ActiveX* est un élément de code exécutable (généralement un fichier ocx qui est empaqueté dans un fichier CAB) qui est installé et exécuté par le biais de Windows Internet Explorer. Vous pouvez créer des contrôles ActiveX pour ajouter des fonctionnalités aux applications Web que vous ne pouvez pas facilement obtenir en utilisant du code HTML standard ou un script simple.

L'installation des contrôles ActiveX devient un problème de compatibilité lorsque votre migration vers Windows 7 inclut une transition vers les utilisateurs standard. Ce type de transition est une meilleure pratique courante dans laquelle les professionnels de l’informatique déplacent leur environnement vers un [compte d’utilisateur standard](https://support.microsoft.com/hub/4338813/windows-help). Cette transition n’est pas obligatoire pour le déploiement de Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>Installation d’un contrôle ActiveX

Les contrôles ActiveX ont un modèle de déploiement téléchargement et exécution simple. Les contrôles ActiveX sont installés et exécutés par le biais de l’élément **objet** html. L’attribut **COdebase** de cet élément indique à Internet Explorer (à l’aide d’une URL) où obtenir le contrôle s’il n’est pas déjà installé sur l’ordinateur de l’utilisateur. Dans ce cas, Internet Explorer télécharge le package d’installation associé, effectue une vérification de confiance sur l’objet et invite l’utilisateur à l’autorisation d’installation dans Internet Explorer.

Pendant l’installation, la page de rendu s’inscrit et exécute le contrôle. Une fois le contrôle installé, tous les utilisateurs standard peuvent exécuter le contrôle. Ce mécanisme simple de distribution et d’exécution offre un moyen simple de distribuer vos composants aux utilisateurs de votre application Web. Toutefois, les utilisateurs de comptes standard ne peuvent pas installer directement les contrôles ActiveX par ordinateur et ils peuvent avoir besoin de privilèges d’administrateur pour terminer l’installation.

## <a name="activex-installer-service-axis"></a>Service d’installation ActiveX (axe)

Le service d’installation ActiveX (AXIS) vous permet de déployer des contrôles ActiveX à l’aide de stratégie de groupe sur les ordinateurs d’une organisation. Vous pouvez configurer AXIS en stratégie de groupe paramètres, que vous pouvez modifier à l’aide de la Console de gestion des stratégies de groupe (GPMC) ou de l’éditeur de stratégie de groupe local.

Il existe deux paramètres de stratégie pour AXIS :

-   Le paramètre de stratégie sites d’installation approuvés pour les contrôles ActiveX est constitué d’une liste de sites d’installation approuvés, que l’axe utilise pour déterminer si un contrôle ActiveX peut être installé.
-   Le paramètre de stratégie stratégie d’installation ActiveX pour les sites dans les zones approuvées identifie la manière dont les zones de sites de confiance peuvent être utilisées pour installer des contrôles ActiveX.

Lorsqu’un site Web tente d’installer un contrôle ActiveX, l’axe vérifie si l’URL du site Web est répertoriée dans la liste des sites d’installation approuvés ou dans le cadre de la zone des sites de confiance. Si le site se trouve dans l’une de ces listes, l’axe s’assure que le site répond aux exigences définies par la stratégie. Si le site et le contrôle ActiveX répondent à toutes les exigences des paramètres de stratégie, le contrôle est installé. Pour plus d'informations, consultez [Administration du service d'installation ActiveX dans Windows 7](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
