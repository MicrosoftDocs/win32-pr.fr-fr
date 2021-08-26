---
description: WMI fournit une interface uniforme pour les applications ou les scripts locaux ou distants qui obtiennent des données de gestion à partir d’un système informatique, d’un réseau ou d’une entreprise.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Architecture WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e261459785fa4e0ccdce7337df788de007c6f335799bbe4778e80f551f5e519e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995522"
---
# <a name="wmi-architecture"></a>Architecture WMI

WMI fournit une interface uniforme pour les applications ou les scripts locaux ou distants qui obtiennent des données de gestion à partir d’un système informatique, d’un réseau ou d’une entreprise. L’interface uniforme est conçue de telle sorte que les applications et les scripts du client WMI n’ont pas besoin d’appeler une grande variété d’interfaces de programmation d’applications (API) du système d’exploitation. de nombreuses api ne peuvent pas être appelées par des clients automation, comme des scripts ou des applications Visual Basic. Les autres API n’effectuent pas d’appels aux ordinateurs distants.

Pour obtenir des données à partir de WMI, écrivez un script client ou une application qui accède aux [classes WMI](wmi-classes.md) ou fournissent des données à WMI en écrivant un [*fournisseur WMI*](gloss-p.md). Pour plus d’informations, consultez [utilisation de WMI](using-wmi.md).

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Objets, consommateurs et infrastructure de WMI

Le diagramme suivant montre la relation entre l’infrastructure WMI et les fournisseurs WMI et les objets gérés, et elle présente également la relation entre l’infrastructure WMI et les consommateurs WMI.

![relation entre l’infrastructure WMI, les fournisseurs WMI et les objets gérés](images/wmi-architecture.png)

## <a name="wmi-components"></a>Composants WMI

La liste suivante décrit les principaux composants WMI :

-   Objets gérés et fournisseurs WMI

    Un fournisseur WMI est un objet COM qui surveille un ou plusieurs [*objets managés*](gloss-m.md) pour WMI. Un objet géré est un composant d’entreprise logique ou physique, tel qu’un lecteur de disque dur, une carte réseau, un système de base de données, un système d’exploitation, un processus ou un service.

    Semblable à un pilote, un fournisseur fournit WMI avec les données d’un objet géré et gère les messages de WMI à l’objet managé. Les fournisseurs WMI se composent d’un fichier DLL et d’un fichier [*format MOF (MOF)*](gloss-m.md) qui définit les classes pour lesquelles le fournisseur retourne des données et effectue des opérations. Les fournisseurs, comme les applications WMI C++, utilisent l' [API com pour WMI](com-api-for-wmi.md). Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).

    Un exemple de fournisseur est le [fournisseur de Registre](/previous-versions/windows/desktop/regprov/system-registry-provider)préinstallé, qui accède aux données dans le registre système. Le fournisseur de registre a une [*classe WMI*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), avec de nombreuses méthodes, mais pas de propriétés. D’autres fournisseurs préinstallés, tels que le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider), ont généralement des classes avec de nombreuses propriétés, mais peu de méthodes, telles que le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou le [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Le fichier DLL du fournisseur de Registre, Stdprov.dll, contient le code qui retourne dynamiquement les données lorsqu’elles sont demandées par des scripts ou des applications clients.

    Les fichiers MOF et DLL WMI se trouvent dans% WINDIR \\ % system32 \\ WBEM, avec les [outils de Command-Line WMI](wmi-command-line-tools.md), tels que [**Winmgmt.exe**](winmgmt.md) et [**Mofcomp.exe**](mofcomp.md). Les classes de fournisseur, telles que [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), sont définies dans les fichiers MOF, puis compilées dans le référentiel WMI au démarrage du système.

-   [Infrastructure WMI](wmi-infrastructure.md)

    l’infrastructure wmi est un composant du système d’exploitation Microsoft Windows connu en tant que service WMI (winmgmt). L’infrastructure WMI a deux composants : le noyau WMI et l' [*espace de stockage WMI*](gloss-w.md).

    Le référentiel WMI est organisé par des espaces de [*noms*](gloss-n.md)WMI. Le service WMI crée des espaces de noms tels que la racine \\ par défaut, le \\ cimv2 racine et l' \\ abonnement racine au démarrage du système, et préinstalle un ensemble par défaut de définitions de classe, y compris les [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider), les [classes système WMI](wmi-system-classes.md)et d’autres. Les espaces de noms restants trouvés sur votre système sont créés par des fournisseurs pour d’autres parties du système d’exploitation ou des produits. Pour plus d’informations et pour obtenir la liste des fournisseurs WMI qui se trouvent dans la plupart des versions de système d’exploitation, consultez [fournisseurs WMI](wmi-providers.md).

    Le service WMI joue le rôle d’intermédiaire entre les fournisseurs, les applications de gestion et l’espace de stockage WMI. Seules les données statiques relatives aux objets sont stockées dans le référentiel, par exemple les classes définies par les fournisseurs. WMI obtient la plupart des données de manière dynamique à partir du fournisseur lorsqu’un client le demande. Vous pouvez également configurer des abonnements pour recevoir des notifications d’événements d’un fournisseur. Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md).

-   Consommateurs WMI

    Un consommateur WMI est un script ou une application de gestion qui interagit avec l’infrastructure WMI. Une application de gestion peut interroger, énumérer des données, exécuter des méthodes de fournisseur ou s’abonner à des événements en appelant l' [API com pour WMI](com-api-for-wmi.md) ou l' [API de script pour WMI](scripting-api-for-wmi.md). Les seules données ou actions disponibles pour un objet géré, comme un lecteur de disque ou un service, sont celles fournies par un fournisseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> <dt>

[Création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Fourniture de données à WMI](providing-data-to-wmi.md)
</dt> <dt>

[Classes WMI](wmi-classes.md)
</dt> <dt>

[Événements d’analyse](monitoring-events.md)
</dt> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 
