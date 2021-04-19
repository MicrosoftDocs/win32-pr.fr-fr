---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 223cfe51-8b1d-4965-b7b1-acc3cd5619f0
ms.tgt_platform: multiple
title: S (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48473c58a1c9aae3f3c9e67f7723167b46df0285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521970"
---
# <a name="s-wmi"></a>S (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [e](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) S [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_schema"></span><span id="WMI.GLOSS_SCHEMA"></span>**schéma**
</dt> <dd>

Collection de définitions de classe qui décrivent des [*objets managés*](gloss-m.md) dans un environnement spécifique.

</dd> <dt>

<span id="wmi.gloss_security_descriptor"></span><span id="WMI.GLOSS_SECURITY_DESCRIPTOR"></span>**descripteur de sécurité**
</dt> <dd>

Structure de données qui contient les informations de sécurité pour un objet sécurisable, tel qu’un partage, un fichier, un récepteur ou un filtre d’événement.

</dd> <dt>

<span id="wmi.gloss_security_identifier"></span><span id="WMI.GLOSS_SECURITY_IDENTIFIER"></span>**identificateur de sécurité (SID)**
</dt> <dd>

Structure de données qui identifie les comptes d’utilisateurs, de groupes et d’ordinateurs.

</dd> <dt>

<span id="wmi.gloss_semi_synchronous"></span><span id="WMI.GLOSS_SEMI_SYNCHRONOUS"></span>**semi synchrone**
</dt> <dd>

Consultez *méthode semi-synchrone*.

</dd> <dt>

<span id="wmi.gloss_semi__synchronous"></span><span id="WMI.GLOSS_SEMI__SYNCHRONOUS"></span>**semi-synchrone**
</dt> <dd>

Consultez *méthode semi-synchrone*.

</dd> <dt>

<span id="wmi.gloss_semisynchronous"></span><span id="WMI.GLOSS_SEMISYNCHRONOUS"></span>**méthode semi-synchrone**
</dt> <dd>

Un appel de méthode qui retourne immédiatement et permet à l’application ou au script d’énumérer les objets retournés en tant que collection.

</dd> <dt>

<span id="gloss_servicesid"></span><span id="GLOSS_SERVICESID"></span>**SID de service**
</dt> <dd>

Un *sid* unique créé pour chaque contexte de sécurité ; autrement dit, un pour « LocalService » et un pour « NetworkService ». Seul le *SID du service* dispose d’autorisations sur les ressources, telles que les threads et les événements, qui sont créés par le processus hôte du fournisseur WMI (wmiprvse.exe).

</dd> <dt>

<span id="wmi.gloss_sid"></span><span id="WMI.GLOSS_SID"></span>**SID**
</dt> <dd>

Consultez *identificateur de sécurité*.

</dd> <dt>

<span id="wmi.gloss_singleton_class"></span><span id="WMI.GLOSS_SINGLETON_CLASS"></span>**Singleton, classe**
</dt> <dd>

Classe WMI qui prend en charge une seule instance.

</dd> <dt>

<span id="wmi.gloss_sink"></span><span id="WMI.GLOSS_SINK"></span>**puits**
</dt> <dd>

Objet COM qui agit comme destination de remise physique pour les résultats d’une opération asynchrone ou d’une notification d’événement. Un récepteur implémenté par un [*consommateur permanent*](gloss-p.md) prend en charge l’interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Un récepteur implémenté par un [*consommateur temporaire*](gloss-t.md) ou des applications qui effectuent des appels asynchrones prend en charge l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .

Les clients de script peuvent utiliser l’objet [**SWbemSink**](swbemsink.md) et les événements, tels que [**OnObjectReady**](swbemsink-onobjectready.md), pour recevoir des rappels résultant d’appels asynchrones.

</dd> <dt>

<span id="wmi.gloss_standard_consumer"></span><span id="WMI.GLOSS_STANDARD_CONSUMER"></span>**consommateur standard**
</dt> <dd>

[*Consommateurs permanents*](gloss-p.md) préinstallés qui exécutent une action, par exemple l’envoi d’un message électronique ou l’écriture dans un journal lorsqu’il est configuré par un fichier ou un script [*format MOF (MOF)*](gloss-m.md) .

</dd> <dt>

<span id="wmi.gloss_standard_provider"></span><span id="WMI.GLOSS_STANDARD_PROVIDER"></span>**fournisseur standard**
</dt> <dd>

[*Fournisseur*](gloss-p.md) intégré à WMI, qui est différent d’un fournisseur tiers ou personnalisé.

</dd> <dt>

<span id="wmi.gloss_standard_qualifier"></span><span id="WMI.GLOSS_STANDARD_QUALIFIER"></span>**qualificateur standard**
</dt> <dd>

[*Qualificateur*](gloss-q.md) que le [*Gestionnaire d’objets CIMOM*](gloss-c.md) attache automatiquement à une classe, une instance, une propriété, une méthode ou un paramètre d’une méthode.

</dd> <dt>

<span id="wmi.gloss_standard_schema"></span><span id="WMI.GLOSS_STANDARD_SCHEMA"></span>**schéma standard**
</dt> <dd>

Une infrastructure conceptuelle commune qui organise et met en relation les classes qui représentent l’état opérationnel actuel d’un système, d’un réseau ou d’une application. La [*DMTF (Distributed Management Task Force)*](gloss-d.md) définit le schéma standard dans le [*Common Information Model (CIM)*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_static_class"></span><span id="WMI.GLOSS_STATIC_CLASS"></span>**classe statique**
</dt> <dd>

Définition de classe CIM qui change rarement et qui est stockée dans le [*référentiel CIM*](gloss-c.md) jusqu’à ce qu’elle soit supprimée explicitement. La [*Gestionnaire d’objets CIMOM*](gloss-c.md) peut fournir une définition d’une classe statique sans [*fournisseur*](gloss-p.md). Une classe statique peut prendre en charge des [*instances*](gloss-d.md) *statiques* ou dynamiques.

</dd> <dt>

<span id="wmi.gloss_static_instance"></span><span id="WMI.GLOSS_STATIC_INSTANCE"></span>**instance statique**
</dt> <dd>

Instance d’une classe CIM qui est stockée de manière permanente dans le [*référentiel CIM*](gloss-c.md) et reste valide jusqu’à ce qu’elle soit supprimée explicitement, même entre les redémarrages du système.

</dd> <dt>

<span id="wmi.gloss_static_method"></span><span id="WMI.GLOSS_STATIC_METHOD"></span>**méthode statique**
</dt> <dd>

Méthode définie dans une classe CIM qui est exécutée en extrayant la définition de classe au lieu de récupérer une instance de la classe.

</dd> <dt>

<span id="wmi.gloss_subschema"></span><span id="WMI.GLOSS_SUBSCHEMA"></span>**sous-schéma**
</dt> <dd>

Partie d’un *schéma* qui appartient à une organisation spécifique. [*Win32schema*](gloss-w.md) est un exemple de sous-schéma.

</dd> <dt>

<span id="wmi.gloss_system_class"></span><span id="WMI.GLOSS_SYSTEM_CLASS"></span>**classe système**
</dt> <dd>

Classe que le [*Gestionnaire d’objets CIMOM*](gloss-c.md) définit pour prendre en charge les fonctionnalités principales telles que la notification d’événements, la sécurité et la localisation. Une classe système est définie automatiquement dans chaque [*espace de noms*](gloss-n.md). Une classe système dérive de la classe de base abstraite [**\_ \_ SystemClass**](--systemclass.md).

</dd> <dt>

<span id="wmi.gloss_system_monitor"></span><span id="WMI.GLOSS_SYSTEM_MONITOR"></span>**Moniteur système**
</dt> <dd>

Utilitaire (CIM) qui est l’interface graphique utilisateur pour l’analyse des performances.

</dd> <dt>

<span id="wmi.gloss_system_property"></span><span id="WMI.GLOSS_SYSTEM_PROPERTY"></span>**propriété système**
</dt> <dd>

Propriété que le [*Gestionnaire d’objets CIMOM*](gloss-c.md) définit pour fournir des informations qui s’appliquent à chaque classe, par exemple, le nom, la dérivation et l' [*espace de noms*](gloss-n.md).

</dd> </dl>

 

 



