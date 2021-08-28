---
description: Un fournisseur est un objet COM (Component Object Model) qui joue le rôle d’intermédiaire entre WMI et un objet géré.
ms.assetid: a4f537ba-9081-43b4-acff-4d206de3d9d7
ms.tgt_platform: multiple
title: Développement d’un fournisseur WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed313af816d48929ae120867f11b7973ff6adf0616f2635e424f890500d67011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924813"
---
# <a name="developing-a-wmi-provider"></a>Développement d’un fournisseur WMI

Un fournisseur est un objet COM (Component Object Model) qui joue le rôle d’intermédiaire entre WMI et un objet géré. Par exemple, lorsqu’une application ou un script demande des données de disque à l’aide de la classe [**\_ LogicalDisk WMI Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , les données sont obtenues de manière dynamique via le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider)préinstallé.

Si vous souhaitez fournir des données via WMI à d’autres applications, vous pouvez créer un fournisseur de code non géré en écrivant un serveur COM ou via les **assistants WMI ATL** dans Visual Studio. Vous pouvez écrire un fournisseur de code managé à l’aide de WMI dans l' .NET Framework. Les rubriques de cette section décrivent le processus d’écriture d’un fournisseur COM non managé.

> [!Note]  
> Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction [**\# pragma AutoRecover**](pragma-autorecover.md) de préprocesseur dans votre fichier format MOF (MOF).

 

Un fournisseur se compose de classes définies dans le schéma [*format MOF (MOF)*](gloss-m.md) et d’un fichier dll qui exécute les fonctions du fournisseur. Par exemple, le fichier MOF qui définit les classes du fournisseur Win32 est CIMWin32. mof et la DLL est CIMWin32.dll, tous deux se trouvent dans% windir% \\ system32 \\ WBEM.

Le schéma MOF du fournisseur peut contenir plusieurs types de fournisseurs. Par exemple, le [fournisseur du journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider) possède des types d’instance, de méthode et de fournisseur d’événements dans un fichier MOF nommé ntevt. mof. Il est recommandé que toutes les classes et tous les schémas d’inscription des fournisseurs associés soient assemblés dans un seul fichier, plutôt que de créer un fichier par classe.

En plus d’utiliser des fournisseurs préinstallés, vous pouvez créer votre propre fournisseur pour fournir des informations sur un périphérique matériel ou les opérations du logiciel.

Le tableau suivant répertorie les tâches de base qui créent un fournisseur.



| Tâche                                                                                                                                                            | Description                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)                                                              | Développez un modèle pour les entités que vous souhaitez gérer via WMI et créez un fichier format MOF (MOF) pour décrire le schéma.<br/> |
| [Fourniture de données à WMI en écrivant un fournisseur](supplying-data-to-wmi-by-writing-a-provider.md)                                                                  | Créez le fournisseur le plus basique couplé à WMI.<br/>                                                                                |
| [Incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md)                                                                    | Incluez le fournisseur en tant que composant dans une application s’il ne s’exécute pas tout le temps.<br/>                                         |
| [Inscription d’un fournisseur](registering-a-provider.md)                                                                                                            | Inscrivez le fournisseur auprès de COM et WMI.<br/>                                                                                               |
| [Initialisation d’un fournisseur](initializing-a-provider.md)                                                                                                          | Implémentez les interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .<br/>   |
| [Appels à WMI](making-calls-to-wmi.md)                                                                                                                  | Appeler des interfaces WMI à partir d’un fournisseur.<br/>                                                                                                  |
| [Emprunt de l’identité d’un client](impersonating-a-client.md)                                                                                                            | Définir la sécurité pour accéder à une application cliente.<br/>                                                                                          |
| [Mise à jour d’un fournisseur](updating-a-provider.md)                                                                                                                  | Améliorez le fournisseur en fonction des besoins.<br/>                                                                                                       |
| [Déchargement d’un fournisseur](unloading-a-provider.md)                                                                                                                | Supprimer le fournisseur de la mémoire pendant l’arrêt ou lorsque le fournisseur est inactif.<br/>                                                         |
| [Fournisseurs de débogage](debugging-providers.md) et [classes de dépannage et de configuration du fournisseur](provider-configuration-and-troubleshooting-classes.md) | Déboguez votre fournisseur à l’aide des fonctionnalités fournies par WMI.<br/>                                                                                 |
| [Obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)                                                          | Déterminez si vous avez besoin d’un fournisseur de compatibilité des applications 32 bits ou si le fournisseur 64 bits peut fournir des données aux deux clients.<br/>      |



 

Les rubriques suivantes décrivent les étapes nécessaires pour écrire différents types de fournisseurs :

-   [Écriture d’un fournisseur d’instances](writing-an-instance-provider.md)
-   [Écriture d’un fournisseur de méthode](writing-a-method-provider.md)
-   [Écriture d’un fournisseur d’événements](writing-an-event-provider.md)
-   [Écriture d’un fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md)
-   [Écriture d’un fournisseur de classe](writing-a-class-provider.md)
-   [Écriture d’un fournisseur de propriétés](writing-a-property-provider.md)
-   [Création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

 

