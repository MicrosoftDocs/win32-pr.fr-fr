---
title: Vue d’ensemble du fournisseur WMI DNS
description: un fournisseur est un élément architectural de Windows Management Instrumentation (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, fournisseur WMI, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44103edba64a1f572beef9cff9b8aeb31f02344f172f42b2a7378a6fbf3677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913159"
---
# <a name="dns-wmi-provider-overview"></a>Vue d’ensemble du fournisseur WMI DNS

un fournisseur est un élément architectural de *Windows Management Instrumentation (WMI)*. WMI définit une architecture unifiée pour décrire, accéder et instrumenter des objets. Une partie de cette architecture est une base de données volumineuse de classes WMI utilisée pour effectuer des tâches de gestion à distance sur des objets spécifiques.

Les fournisseurs WMI jouent le rôle d’intermédiaires entre WMI et un ou plusieurs objets gérés. Lorsque WMI reçoit une demande d’une application de gestion pour les données qui ne sont pas disponibles dans le référentiel CIM ou pour les notifications d’événements que WMI ne prend pas en charge, il transfère la demande à un fournisseur. Les fournisseurs renvoient les données et les notifications d’événements pour les objets gérés qui sont spécifiques à leur domaine particulier. Un fournisseur étend le schéma WMI des classes pour permettre à WMI de fonctionner avec de nouveaux types d’objets. Le fournisseur WMI DNS définit des classes pour l’interrogation et la configuration d’un serveur DNS, ainsi que des zones DNS et des enregistrements DNS associés.

Le fournisseur WMI DNS expose un certain nombre d’objets DNS aux clients, y compris le serveur DNS, le domaine DNS et les objets de ressource DNS. Grâce à ces objets, les clients sont en mesure d’effectuer des activités de gestion DNS.

À l’aide du fournisseur WMI DNS, vous pouvez créer vos propres outils pour effectuer la plupart des tâches d’administration de serveur DNS. Par exemple, vous pouvez créer, supprimer et afficher des zones et des enregistrements. réinitialiser les propriétés de serveur et de zone ; et effectuent des opérations d’administration de routine, telles que la mise à jour de la zone, le rechargement de la zone, l’actualisation de la zone, l’écriture de la zone dans un fichier ou un Active Directory, l’interruption et la reprise de la zone, l’effacement du cache, l’arrêt et le démarrage du service DNS, ainsi que l’affichage des statistiques.

Le fournisseur WMI DNS possède un ensemble de comportements uniques introuvables dans d’autres fournisseurs. Pour plus d’informations sur les classes, consultez la [Référence du fournisseur WMI DNS](dns-wmi-provider-reference.md) .

 

 




