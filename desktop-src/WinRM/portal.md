---
title: gestion à distance de Windows
description: Windows la gestion à distance (Windows Remote Management) est l’implémentation Microsoft du protocole WS-Management, un protocole SOAP standard, compatible avec un pare-feu qui permet l’interopérabilité du matériel et des systèmes d’exploitation de différents fournisseurs.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows Gestion à distance (WinRM), page de démarrage
- Gestion des services Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c816e3f7092fc7825407497793ed529df13cf9115426b63e4b535bd019f81df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858759"
---
# <a name="windows-remote-management"></a>gestion à distance de Windows

## <a name="purpose"></a>Objectif

La gestion à distance de Windows (WinRM) est l’implémentation Microsoft du [protocole Gestion des services web](ws-management-protocol.md), un protocole SOAP (Simple Object Access Protocol) standard, compatible avec un pare-feu qui permet l’interaction entre du matériel et des systèmes d’exploitation de différents fabricants.

La spécification de protocole WS-Management permet aux systèmes d’accéder et d’échanger des informations de gestion à travers une infrastructure informatique. WinRM et l' [*Interface de gestion de plateforme intelligente (IPMI)*](windows-remote-management-glossary.md), ainsi que le [collecteur d’événements](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) sont des composants des fonctionnalités de gestion du [matériel Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .

## <a name="where-applicable"></a>Le cas échéant

vous pouvez utiliser les objets de script winrm, l’outil en ligne de commande winrm ou l’outil en ligne de commande Windows de l’interpréteur de commandes à distance WinRS pour obtenir des données de gestion à partir d’ordinateurs locaux et distants qui peuvent avoir des [*contrôleurs de gestion*](windows-remote-management-glossary.md)de la carte de contrôleurs bmc. si l’ordinateur exécute une version de système d’exploitation basée sur Windows qui comprend WinRM, les données de gestion sont fournies par [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).

Vous pouvez également obtenir des données système et matériel d’implémentations du protocole Gestion des services Web qui exécutent des systèmes d’exploitation autres que Windows dans votre entreprise. WinRM établit une session avec un ordinateur distant via le protocole Gestion des services Web SOAP plutôt que via DCOM, comme le fait WMI. Les données retournées au protocole Gestion des services Web sont au format XML plutôt que des objets.

Le fournisseur WMI de l' [interface IPMI (Intelligent Platform Management Interface)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) est un fournisseur WMI standard avec des classes qui obtiennent les données de capteur BMC des ordinateurs équipés du matériel approprié. Les données IPMI sont accessibles via l’API de script WinRM, les [scripts](/windows/desktop/WmiSdk/scripting-api-for-wmi)WMI ou les API [com](/windows/desktop/WmiSdk/com-api-for-wmi) .

## <a name="developer-audience"></a>Développeurs concernés

l’audience du développeur est l’Pro qui écrit des scripts pour automatiser la gestion des serveurs ou le développeur ISV qui obtient des données pour les applications de gestion.

## <a name="run-time-requirements"></a>Conditions d’exécution

WinRM fait partie du système d’exploitation. Toutefois, pour obtenir des données à partir d’ordinateurs distants, vous devez configurer un [*écouteur*](windows-remote-management-glossary.md#l)WinRM. pour plus d’informations, consultez [Installation et Configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md). Si un contrôleur BMC est détecté au démarrage du système, le fournisseur IPMI se charge ; Sinon, les objets de script WinRM et l’outil en ligne de commande WinRM sont toujours disponibles.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dd>

Liaison à la spécification du protocole WS-Management public, à l’architecture WinRM, à la relation avec WMI, à la gestion du matériel avec le fournisseur IPMI, à la configuration et à l’installation.

</dd> <dt>

[utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dd>

Prise en main de l’API de script WinRM et de la gestion du matériel.

</dd> <dt>

[Windows Informations de référence sur la gestion à distance](windows-remote-management-reference.md)
</dt> <dd>

Liste des interfaces de script définies par Microsoft Web Services for Management (WS-Management) Automation et les définitions de classe des classes WMI créées par le fournisseur IPMI et les classes qui communiquent avec le pilote IPMI pour obtenir les données du contrôleur de gestion de la [carte de gestion (BMC)](windows-remote-management-glossary.md) .

</dd> </dl>

 

 