---
description: WMI s’exécute en tant que service portant le nom d’affichage &\# 0034 ; Windows Management Instrumentation&\# 0034 ; et le nom de service &\# 0034 ; winmgmt&\# 0034 ;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Démarrage et arrêt du service WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b22524d356bad5f23f4ca1cc8a3e7c68e69fd83f0dc38e64eba70bc1812436f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315007"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Démarrage et arrêt du service WMI

WMI s’exécute en tant que service portant le nom d’affichage « Windows Management Instrumentation » et le nom de service « winmgmt ». WMI s’exécute automatiquement au démarrage du système sous le compte LocalSystem. Si WMI n’est pas en cours d’exécution, il démarre automatiquement lorsque la première application ou le script de gestion demande une connexion à un espace de noms WMI.

Plusieurs autres services dépendent du service WMI, en fonction de la version du système d’exploitation exécutée par le système.

## <a name="starting-winmgmt-service"></a>Démarrage du service WinMgmt

La procédure suivante décrit comment démarrer le service WMI.

**Pour démarrer le service WinMgmt**

1.  À l’invite de commandes, entrez **net** **Start** **winmgmt** \[ */<switch>* \] .

    Pour plus d’informations sur les commutateurs disponibles, consultez [winmgmt](winmgmt.md). Vous utilisez le compte administrateur intégré ou un compte dans le groupe administrateurs s’exécutant avec des droits élevés pour démarrer le service WMI. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).

2.  les autres services qui dépendent du service WMI, tels que l’hôte de l’Agent SMS ou le pare-feu Windows, ne sont pas redémarrés automatiquement.

## <a name="stopping-winmgmt-service"></a>Arrêt du service WinMgmt

La procédure suivante décrit comment arrêter le service WMI.

**Pour arrêter le service WinMgmt**

1.  À l’invite de commandes, entrez **net stop winmgmt**.

2.  d’autres services qui dépendent du service WMI s’arrêtent également, tels que l’hôte de l’Agent SMS ou le pare-feu Windows.

## <a name="examples"></a>Exemples

La Galerie TechNet contient le [script de la surveillance du service WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), qui décrit comment arrêter par programmation et redémarrer le service WinMgmt avec PowerShell.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des outils de Command-Line WMI](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



