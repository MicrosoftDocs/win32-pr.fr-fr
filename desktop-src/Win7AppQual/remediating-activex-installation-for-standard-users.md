---
description: résolution des problèmes de compatibilité de l’Installation de ActiveX pour les utilisateurs Standard
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: résolution des problèmes de compatibilité de l’Installation de ActiveX pour les utilisateurs Standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88b26ebd0c6e4887a8a304aeab725b176ee04a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531536"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>résolution des problèmes de compatibilité de l’Installation de ActiveX pour les utilisateurs Standard

pour développer un environnement de bureau sécurisé, vous devez atténuer les menaces des contrôles de ActiveX malveillants et fournir un niveau approprié de compatibilité des applications dans votre environnement. un *contrôle de ActiveX* est un élément de code exécutable (généralement un fichier OCX qui est empaqueté dans un fichier cab) qui est installé et exécuté via Windows Internet Explorer. vous pouvez créer des contrôles de ActiveX pour ajouter des fonctionnalités aux applications web que vous ne pouvez pas facilement obtenir en utilisant du code HTML standard ou un script simple.

L'installation des contrôles ActiveX devient un problème de compatibilité lorsque votre migration vers Windows 7 inclut une transition vers les utilisateurs standard. Ce type de transition est une meilleure pratique courante dans laquelle les professionnels de l’informatique déplacent leur environnement vers un [compte d’utilisateur standard](https://support.microsoft.com/hub/4338813/windows-help). cette transition n’est pas obligatoire pour le déploiement d’Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>ActiveX Installation du contrôle

les contrôles ActiveX ont un modèle de déploiement téléchargement et exécution simple. les contrôles ActiveX sont installés et exécutés par le biais de l’élément **objet** HTML. L’attribut **COdebase** de cet élément indique à Internet Explorer (à l’aide d’une URL) où obtenir le contrôle s’il n’est pas déjà installé sur l’ordinateur de l’utilisateur. Dans ce cas, Internet Explorer télécharge le package d’installation associé, effectue une vérification de confiance sur l’objet et invite l’utilisateur à l’autorisation d’installation dans Internet Explorer.

Pendant l’installation, la page de rendu s’inscrit et exécute le contrôle. Une fois le contrôle installé, tous les utilisateurs standard peuvent exécuter le contrôle. Ce mécanisme simple de distribution et d’exécution offre un moyen simple de distribuer vos composants aux utilisateurs de votre application Web. toutefois, les utilisateurs de comptes standard ne peuvent pas installer directement les contrôles de ActiveX par ordinateur et ils peuvent nécessiter des privilèges d’administrateur pour terminer l’installation.

## <a name="activex-installer-service-axis"></a>ActiveX Service d’installation (axe)

le Service d’installation ActiveX (axe) vous permet de déployer des contrôles de ActiveX à l’aide de stratégie de groupe sur les ordinateurs d’une organisation. Vous pouvez configurer AXIS en stratégie de groupe paramètres, que vous pouvez modifier à l’aide de la Console de gestion des stratégies de groupe (GPMC) ou de l’éditeur de stratégie de groupe local.

Il existe deux paramètres de stratégie pour AXIS :

-   le paramètre de stratégie sites d’installation approuvés pour les contrôles de ActiveX se compose d’une liste de sites d’installation approuvés, que l’axe utilise pour déterminer si un contrôle ActiveX peut être installé.
-   le paramètre de stratégie ActiveX la stratégie d’installation pour les sites dans les zones approuvées identifie la manière dont les zones sites de confiance peuvent être utilisées pour installer des contrôles ActiveX.

lorsqu’un site web tente d’installer un contrôle de ActiveX, l’axe vérifie si l’URL du site web est répertoriée dans la liste des sites d’installation approuvés ou dans le cadre de la zone des sites de confiance. Si le site se trouve dans l’une de ces listes, l’axe s’assure que le site répond aux exigences définies par la stratégie. Si le site et le contrôle ActiveX répondent à toutes les exigences des paramètres de stratégie, le contrôle est installé. Pour plus d'informations, consultez [Administration du service d'installation ActiveX dans Windows 7](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
