---
description: WMI s’exécute dans le cadre d’un hôte de service partagé avec les ports attribués par le biais de DCOM par défaut. Toutefois, vous pouvez configurer le service WMI pour qu’il s’exécute en tant que seul processus dans un hôte distinct et spécifier un port fixe.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configuration d’un port fixe pour WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b97ee9d0f2f407c0cae2c9c1466a1904cf79eaecb353b94ac11bb3373367ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050247"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Configuration d’un port fixe pour WMI

WMI s’exécute dans le cadre d’un hôte de service partagé avec les ports attribués par le biais de DCOM par défaut. Toutefois, vous pouvez configurer le service WMI pour qu’il s’exécute en tant que seul processus dans un hôte distinct et spécifier un port fixe.

La procédure suivante est une installation automatisée pour permettre à WMI d’avoir un port fixe. La procédure utilise l’outil en ligne de commande [**winmgmt**](winmgmt.md) .

**Pour configurer un port fixe pour WMI**

1.  À l’invite de commandes, tapez **winmgmt-standalonehost**
2.  arrêtez le service WMI en tapant la commande **net stop « Windows Management Instrumentation »**, ou utilisez le nom abrégé **net stop winmgmt**
3.  redémarrez le service WMI dans un nouvel hôte de service en tapant **net start « Windows Management Instrumentation »** ou **net start winmgmt**
4.  Établissez un nouveau numéro de port pour le service WMI en tapant **netsh firewall Add ouverture TCP 24158 WMIFixedPort**

Pour annuler les modifications apportées à WMI, tapez **winmgmt/sharedhost**, puis arrêtez et redémarrez le service WinMgmt.

## <a name="examples"></a>Exemples

Pour obtenir un script qui configure un port fixe pour WMI, consultez l' [exemple de code](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )de la Galerie de scripts suivant.

ou un exemple de code PowerShell qui active ou désactive les paramètres de port WMI, reportez-vous à l’exemple [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) sur la Galerie technet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Résolution des problèmes de connexions WMI distantes](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Hébergement et sécurité du fournisseur](provider-hosting-and-security.md)
</dt> </dl>

 

 



