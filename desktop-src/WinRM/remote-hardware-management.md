---
title: Gestion matérielle à distance
description: Gestion matérielle à distance
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Gestion matérielle à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bbb470d513b49d2158865c4c42051cc16856ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727396"
---
# <a name="remote-hardware-management"></a>Gestion matérielle à distance

Windows Remote Management la gestion du matériel est destinée à réduire les coûts d’administration informatique globaux en fournissant la surveillance et le contrôle des composants matériels distants, en particulier avant le démarrage du système et après une défaillance du système d’exploitation.

Les fabricants d’ordinateurs OEM ont développé une architecture commune pour répondre au besoin de gestion du matériel. Un élément important de cette architecture est le [*contrôleur BMC (Baseboard Management Controller*](windows-remote-management-glossary.md) ). Un contrôleur BMC est un appareil spécialisé qui surveille l’état de l’ordinateur serveur. Le BMC permet de contrôler à distance le matériel du serveur, récupère les données d’État et reçoit des notifications sur les erreurs critiques et les autres changements d’État du matériel. Un script ou une application qui analyse un serveur distant peut obtenir des données du serveur [*en interne*](windows-remote-management-glossary.md), via le système d’exploitation distant ou [*hors bande*](windows-remote-management-glossary.md), directement à partir du BMC.

Un contrôleur BMC a des capteurs qui peuvent détecter, par exemple, si l’ordinateur serveur est en surchauffe ou lorsque la tension est en dehors de la plage acceptable. Il existe plusieurs normes pour définir l’architecture de BMC. L' [*interface de gestion de plateforme intelligente (IPMI)*](windows-remote-management-glossary.md) est une norme qui est fréquemment utilisée. Toutefois, malgré la norme IPMI, l’accès à la gestion du matériel serveur est propriétaire et requiert l’utilisation d’outils de gestion fournis par les fabricants d’ordinateurs OEM. En outre, l’accès à distance à un contrôleur BMC est fourni à l’aide d’un protocole câblé spécialisé, RMCP (Remote Management Control Protocol), qui dispose de mécanismes de sécurité non standard pour l’authentification de l’accès.

Le [fournisseur Microsoft IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) et le pilote IPMI vous permettent d’obtenir des données BMC à partir d’ordinateurs serveurs distants via un fournisseur WMI standard avec des [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI. Bien que vous puissiez écrire un script WMI normal qui obtient des données distantes via DCOM, dans de nombreux cas, la méthode recommandée pour obtenir des données IPMI consiste à utiliser l’utilitaire de ligne de commande **WinRM** ou l' [API de script WINRM](winrm-scripting-api.md) ou l' [API WinRM C++](winrm-c---api.md). L’utilitaire WinRM et les API du service WinRM s’appuient sur le protocole WS-Management et peuvent obtenir des données IPMI à partir d’un ordinateur local ou distant sans utiliser DCOM.

Le contrôleur BMC possède également une base de données d’événements appelée Journal des événements système (SEL) qui enregistre les événements sur l’ordinateur analysé. Vous ne pouvez pas vous abonner pour que ces événements soient remis à un script comme vous le pouvez avec les classes d’événements WMI. Toutefois, vous pouvez utiliser l’outil en ligne de commande Wecutil.exe pour vous y abonner. Pour plus d’informations sur l’utilisation de cet outil, à l’invite de commandes, tapez **wecutil/ ?**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Protocole Gestion des services web](ws-management-protocol.md)
</dt> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> </dl>

 

 