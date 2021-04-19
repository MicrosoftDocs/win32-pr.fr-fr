---
description: L’environnement AppContainer est un environnement d’exécution de processus restrictif qui peut être utilisé pour les applications héritées afin de garantir la sécurité des ressources.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: AppContainer pour les applications héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b25ea292bdb8935375e50f669d17deb7efaef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535635"
---
# <a name="appcontainer-for-legacy-applications"></a>AppContainer pour les applications héritées

L’environnement AppContainer est un environnement d’exécution de processus restrictif qui peut être utilisé pour les applications héritées afin de garantir la sécurité des ressources. Une application s’exécutant dans un AppContainer peut accéder uniquement aux ressources qui lui sont accordées spécifiquement. Par conséquent, les applications implémentées dans un AppContainer ne peuvent pas être piratées pour permettre des actions malveillantes en dehors des ressources affectées limitées.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Avantages de l’utilisation d’un environnement AppContainer

L’environnement AppContainer fournit un sandbox sécurisé des applications. Cela isole l’application de l’accès au matériel, aux fichiers, au registre, aux autres applications, à la connectivité réseau et aux ressources réseau sans autorisation spécifique. Les ressources individuelles peuvent être ciblées sans exposer d’autres ressources. En outre, l’identité de l’utilisateur est protégée à l’aide d’une identité unique qui est une concaténation de l’utilisateur et l’application et les ressources sont accordées à l’aide d’un modèle de privilège minimum. Cela permet d’éviter qu’une application emprunte l’identité de l’utilisateur pour accéder à d’autres ressources.

Pour plus d’informations sur l’utilisation d’AppContainer pour les applications héritées, consultez les rubriques suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Isolation d’AppContainer](appcontainer-isolation.md)<br/>             | L’isolation est l’objectif principal d’un environnement d’exécution AppContainer. En isolant une application des ressources inutiles et d’autres applications, les opportunités de manipulation malveillante sont réduites. L’octroi d’un accès basé sur des privilèges minimaux empêche les applications et les utilisateurs d’accéder aux ressources au-delà de leurs droits. Le contrôle de l’accès aux ressources protège le processus, l’appareil et le réseau.<br/> |
| [Implémentation d’un AppContainer](implementing-an-appcontainer.md)<br/> | Un AppContainer est implémenté en ajoutant de nouvelles informations au jeton de processus, en modifiant [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) afin que tous les objets de liste de contrôle d’accès (ACL) hérités et non modifiés bloquent les demandes d’accès des processus AppContainer par défaut, et les objets de réacl qui doivent être disponibles pour AppContainers.<br/>                                                                                        |



 

 

