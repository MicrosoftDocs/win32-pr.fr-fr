---
description: La communication avec un périphérique réseau à l’aide de l’interface WMI SNMP requiert la configuration des services de l’appareil, du SNMP et de WMI. Les informations contenues dans cette rubrique expliquent comment configurer l’environnement SNMP WMI.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configuration de l’environnement WMI SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320666"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Configuration de l’environnement WMI SNMP

La communication avec un périphérique réseau à l’aide de l’interface WMI SNMP requiert la configuration des services de l’appareil, du SNMP et de WMI. Les informations contenues dans cette rubrique expliquent comment configurer l’environnement SNMP WMI.

Les sections suivantes sont présentées dans cette rubrique :

## <a name="installing-the-snmp-provider"></a>Installation du fournisseur SNMP

Le service SNMP n’est pas activé par défaut. Vous pouvez activer le service SNMP et le fournisseur SNMP WMI via le panneau de configuration. N’oubliez pas que le service SNMP doit être activé et en cours d’exécution pour que le fournisseur SNMP SNMP fonctionne.

À compter de Windows Vista, utilisez la procédure suivante pour installer le fournisseur SNMP.

**Pour installer le fournisseur SNMP**

1.  Dans le **panneau de configuration**, sélectionnez **programmes**.
2.  Sous **programmes et fonctionnalités**, sélectionnez **activer ou désactiver des fonctionnalités Windows**.
3.  Dans la liste des fonctionnalités Windows, faites défiler jusqu’à **fonctionnalité SNMP** , puis développez la liste pour voir le **fournisseur SNMP SNMP**.
4.  Activez la case à cocher du **fournisseur SNMP WMI**. La case à cocher de la **fonctionnalité SNMP** est automatiquement activée, car le fournisseur requiert SNMP.
5.  Cliquez sur **OK**.
6.  À partir d’une invite de commandes ou du menu **Démarrer** , exécutez services. msc et vérifiez que le service SNMP est démarré.

## <a name="creating-an-snmp-namespace"></a>Création d’un espace de noms SNMP

Un espace de noms SNMP définit une vue d’un périphérique réseau.

> [!Note]  
> Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).

 

La procédure suivante décrit comment créer un [*espace de noms*](gloss-n.md)WMI SNMP.

**Pour créer un espace de noms SNMP**

1.  Créez une instance de la classe système d' [**\_ \_ espace de noms**](--namespace.md) en compilant un fichier [*format MOF*](gloss-m.md) . mof ou en utilisant l' [API com pour WMI](com-api-for-wmi.md).

    Pour plus d’informations, consultez [création de hiérarchies dans WMI](creating-hierarchies-within-wmi.md).

2.  Associez les [*qualificateurs*](gloss-q.md) du fournisseur SNMP à la définition de l’espace de noms.

    Les qualificateurs du fournisseur SNMP contiennent des informations de contexte spécifiques à l’implémentation et des propriétés de transport qui définissent la façon dont le fournisseur SNMP accède à un périphérique SNMP. Pour plus d’informations, consultez [**qualificateurs spécifiques au fournisseur SNMP**](qualifiers-specific-to-the-snmp-provider.md).

3.  Utilisez l’outil en ligne de commande [mofcomp](mofcomp.md) pour charger le code MOF dans le référentiel WMI.

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

L’exemple de code MOF suivant définit l' \\ espace de noms SNMP avec un sous-ensemble des qualificateurs qui peuvent être associés à un espace de noms SNMP.

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a>Insertion de données MIB SNMP dans WMI

En tant que fournisseur, le fournisseur SNMP agit comme un pont entre les données SNMP et les classes WMI. Par conséquent, vous devez avoir des classes dans WMI qui représentent différents aspects d’un périphérique SNMP. Pour ce faire, vous devez utiliser le compilateur de module d’informations SNMP ([Smi2smir](smi2smir.md)) pour compiler les informations de gestion SNMP du format SNMP vers les définitions de schéma CIM équivalentes. Vous pouvez ensuite diriger la sortie du compilateur d’informations dans une base de données de schéma SNMP appelée « référentiel d’informations de module SNMP (stockage SMIR) » ou à plusieurs types de fichiers MOF.

Le compilateur s’exécute en mode de ligne de commande, en utilisant un fichier MIB comme entrée. La commande suivante charge le fichier MIB spécifié dans stockage SMIR.

**Smi2smir/a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Configuration des communautés SNMP

En guise de mesure de sécurité, la communauté SNMP « public » n’est pas créée par défaut. Vous pouvez créer la communauté comme décrit dans [paramètres du registre des communautés](/previous-versions/windows/embedded/ms907028(v=msdn.10)). Si vous n’avez pas de communauté, créez la communauté « public » pour accéder au fournisseur SNMP.

## <a name="generating-mof-files-from-mib-files"></a>Génération de fichiers MOF à partir de fichiers MIB

Les commandes suivantes sont un exemple de génération de fichiers MOF à partir des fichiers MIB qui sont installés lors de l’installation du fournisseur SNMP.

**CD** *% windir% \\ system32 \\ WBEM \\ SNMP*

**Smi2smir/g** *... \\ . \\ hostmib. MIB* **>** *hostmib. mof*

**Smi2smir/g** *... \\ . \\ ipforwd. MIB* **>** *ipforwd. mof*

**Smi2smir/g** *... \\ . \\ nipx. MIB* **>** *nipx. mof*

**Smi2smir/g** *... \\ . \\ MIB II \_ .* mib MIB II **>** *\_ . mof*

**Smi2smir/g** *... \\ . \\ lmmib2. MIB* **>** *lmmib2. mof*

**Smi2smir/g** *... \\ . \\ mcastmib. MIB* **>** *mcastmib. mof*

**Smi2smir/g** *... \\ . \\ rfc2571. MIB* **>** *rfc2571. mof*

**Smi2smir/g** *... \\ . \\ wfospf. MIB* **>** *wfospf. mof*

**Smi2smir/g** *... \\ . \\ DHCP. MIB... \\ . \\ msft. MIB* **>** *DHCP. mof*

**Smi2smir/g** *... \\ . \\ WINS. MIB... \\ . \\ msft. MIB* **>** *, WINS. mof*

**Smi2smir/g** *... \\ . \\ mipx. MIB... \\ . \\ msft. MIB* **>** *mipx. mof*

**Smi2smir/g** *... \\ . \\ mripsap. MIB... \\ . \\ msft. MIB* **>** *mripsap. mof*

**Smi2smir/g** *... \\ . \\ msipbtp. MIB... \\ . \\ msft. MIB* **>** *msipbtp. mof*

**Smi2smir/g** *... \\ . \\ msiprip2. MIB... \\ . \\ msft. MIB* **>** *msiprip2. mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Ajout de fichiers MOF SNMP à l’espace de stockage WMI

Les commandes suivantes sont un exemple de la façon d’ajouter les fichiers MOF générés à partir des fichiers MIB à l’espace de stockage WMI. Si vous souhaitez ajouter les fichiers MOF à la liste des fichiers à restaurer automatiquement dans une récupération de [*référentiel WMI*](gloss-w.md) , ajoutez l’indicateur **-AutoRecover** à la fin de chaque commande. Pour plus d’informations sur l’outil de ligne de commande WMI Mofcomp.exe, consultez [**mofcomp**](mofcomp.md).

**mofcomp** *hostmib. mof*

**mofcomp** *ipforwd. mof*

**mofcomp** *nipx. mof*

**mofcomp** *MIB \_ II. mof*

**mofcomp** *lmmib2. mof*

**mofcomp** *mcastmib. mof*

**mofcomp** *rfc2571. mof*

**mofcomp** *wfospf. mof*

**mofcomp** *DHCP. mof*

**mofcomp** *mipx. mof*

**mofcomp** *mripsap. mof*

**mofcomp** *msipbtp. mof*

**mofcomp** *msiprip2. mof*

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux appareils SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 
