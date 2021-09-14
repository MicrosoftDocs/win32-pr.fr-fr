---
description: wmi fournit des données sur Windows objets gérables accessibles via des fournisseurs WMI.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Fourniture de données à WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60df0384bd6f512b931870775067d9d9e6d4077d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216673"
---
# <a name="providing-data-to-wmi"></a>Fourniture de données à WMI

wmi fournit des données sur Windows objets gérables accessibles via des [*fournisseurs*](gloss-p.md)WMI. Un fournisseur récupère les données d’un composant système, tel qu’un processus, ou une application instrumentée, telle que SNMP ou IIS, et transmet ces données via WMI à une application de gestion. Par exemple, lorsqu’une application ou un script demande des informations de traitement à l’aide de la classe de [**\_ processus WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) , les données sont obtenues de manière dynamique via un fournisseur préinstallé.

Les sections suivantes sont présentées dans cette rubrique :

-   [Création d’un modèle pour un objet gérable](#creating-a-model-for-a-manageable-object)
-   [Implémentation d’un modèle pour un objet gérable](#implementing-a-model-for-a-manageable-object)
-   [Détermination d’un type de fournisseur à implémenter](#determining-a-provider-type-to-implement)
-   [Détermination d’un modèle d’hébergement (implémentation) pour un fournisseur](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implémentation d’un fournisseur](#implementing-a-provider)
-   [Inscription d’un fournisseur avec WMI et le système](#registering-a-provider-with-wmi-and-the-system)
-   [Test d’un fournisseur](#testing-a-provider)
-   [Rubriques connexes](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Création d’un modèle pour un objet gérable

Avant de développer un fournisseur, créez un modèle de données pour représenter l’objet gérable à exposer via WMI. Vous planifiez les objets de données que votre fournisseur exposera. Par exemple, si vous envisagez de gérer la résolution d’écran de l’arrière-plan du bureau, vous devez décider comment modéliser le bureau dans un fichier de [*format MOF (MOF)*](gloss-m.md) .

Pour créer un modèle utile :

-   Déterminez les scénarios réels et modélisez les informations qu’un client peut vouloir lire et mettre à jour (par exemple, modifier l’image d’arrière-plan) pour chaque objet gérable. Il s’agit des propriétés de votre classe.
-   Déterminez le type d’action qu’un client peut souhaiter effectuer avec chaque objet gérable. Il s’agit de vos méthodes.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implémentation d’un modèle pour un objet gérable

Pour implémenter un modèle d’objets gérables, créez un fichier MOF contenant une classe WMI qui représente chaque objet. Pour plus d’informations sur la création d’un fichier MOF pour définir des classes WMI, consultez [conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md). L’inscription du fournisseur et de ses classes est généralement incluse dans le fichier MOF, bien qu’il soit possible d’utiliser l' [API com](com-api-for-wmi.md) pour créer des classes et des méthodes. Pour plus d’informations, consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).

> [!Note]  
> Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction [**\# pragma AutoRecover**](pragma-autorecover.md) de préprocesseur dans votre fichier [*format MOF (MOF)*](gloss-m.md) .

 

Après avoir créé le fichier MOF, compilez-le à l’aide de l’outil [**Mofcomp.exe**](mofcomp.md) . Cela vous avertit des erreurs dans votre fichier MOF et ajoute la classe WMI définie dans le fichier MOF à l' [*espace de stockage WMI*](gloss-w.md) afin que la classe puisse être utilisée par un fournisseur.

## <a name="determining-a-provider-type-to-implement"></a>Détermination d’un type de fournisseur à implémenter

WMI prend en charge un certain nombre de types de fournisseurs, ce qui détermine la nature des informations fournies et les opérations prises en charge par les fournisseurs.

Les types de fournisseurs sont les suivants :

-   [*Fournisseur d’instance*](gloss-i.md)
-   [*Fournisseur de méthode*](gloss-m.md)
-   [*Fournisseur de propriétés*](gloss-p.md)
-   Fournisseur de classes
-   [*Fournisseur d’événements*](gloss-e.md)
-   [*Fournisseur de consommateur d’événements*](gloss-e.md)
-   [*Fournisseur d’associations*](gloss-a.md)

La plupart des fournisseurs sont des fournisseurs d’instances et des fournisseurs de méthodes. Un fournisseur d’instances est le fournisseur le plus courant et fournit les instances d’une classe donnée. Un fournisseur de méthode implémente les méthodes d’une ou plusieurs classes. Pour plus d’informations sur les types de fournisseurs, consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Détermination d’un modèle d’hébergement (implémentation) pour un fournisseur

Les fournisseurs WMI sont des binaires implémentés en tant qu’objets COM. Cela signifie que chaque fournisseur a un fichier DLL qui peut être exécuté dans un processus et un contexte de sécurité spécifiques. C’est ce que WMI fait référence en tant que [*modèle d’hébergement*](gloss-h.md). WMI offre différentes manières d’héberger des fournisseurs, mais l’approche la plus courante consiste à utiliser le modèle de fournisseur couplé (exécuté sous le processus WMI) dans le contexte de sécurité NetworkServiceHost. Un fournisseur WMI peut être classé comme étant couplé ou [*découplé*](gloss-d.md).

Le terme fournisseur couplé ou découplé détermine sous quel processus hôte le fournisseur s’exécute en ce qui concerne le processus WMI fourni WMIPRVSE.EXE processus. Il est recommandé de déterminer si les données de gestion que le fournisseur expose et l’API ou l’application sur laquelle il s’appuie sont toujours disponibles dans le système ou non. Si l’API ou l’application sur laquelle le fournisseur s’appuie est toujours disponible (en cours d’exécution sur le système), le fournisseur doit être un fournisseur couplé, sinon, il doit s’agir d’un fournisseur découplé. Pour plus d’informations sur les modèles d’hébergement, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

Pour plus d’informations sur la création d’un fournisseur couplé, consultez [fourniture de données à WMI en écrivant un fournisseur](supplying-data-to-wmi-by-writing-a-provider.md)et pour plus d’informations sur l’incorporation d’un fournisseur découplé dans une application, consultez [incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md).

Les fournisseurs couplés peuvent être décrits comme in-process (in-proc) ou out-of-process (out-of-proc). Lorsqu’un fournisseur couplé est un fournisseur in-proc, il s’exécute sous un processus d’hébergement WMIPRVSE.EXE WMI partagé et est implémenté en tant que serveur COM in-proc (.dll). Lorsqu’un fournisseur est un fournisseur hors processus, il est démarré par WMI à la demande d’un client ou d’un événement, mais il s’exécute en tant que processus séparé et est implémenté en tant qu’exécutable (.exe).

## <a name="implementing-a-provider"></a>Implémentation d’un fournisseur

Un fournisseur peut être implémenté des manières suivantes :

-   À l’aide de l’Assistant ATL dans Visual Studio.

    L’Assistant ATL génère du code fournisseur qui implémente un fournisseur couplé. Lors de l’utilisation de l’Assistant ATL, vous pouvez spécifier que vous souhaitez créer un modèle d’exécution de fournisseur in-proc (.dll) ou out-of-proc (.exe).

-   Définition d’un objet COM pour contenir votre fournisseur.

    Le code du fournisseur est écrit en C++. Pour plus d’informations, consultez [fourniture de données à WMI en écrivant un fournisseur](supplying-data-to-wmi-by-writing-a-provider.md).

-   utilisation des classes de l’espace de noms [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) dans le .NET Framework pour créer un fournisseur à l’aide de code managé. (L’espace de noms **System. Management. Instrumentation** n’est plus pris en charge.)

    Ce processus crée un fournisseur découplé.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Inscription d’un fournisseur avec WMI et le système

avant d’utiliser le fournisseur d’un consommateur, il est important de l’inscrire auprès du système WMI et du sous-système Windows COM.

Un fichier MOF peut contenir plusieurs types de fournisseurs pour les mêmes classes. Le même nom de fournisseur est enregistré sous la forme, par exemple, d’une instance ou d’un fournisseur de méthode. Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).

## <a name="testing-a-provider"></a>Test d’un fournisseur

Lorsque le code du fournisseur est inscrit, il est important de tester correctement le fournisseur à l’aide du fournisseur de différents consommateurs (par exemple, des scripts, du code managé .NET et des consommateurs C++).

Effectuez les tâches suivantes pour tester votre fournisseur :

-   Assurez-vous que votre fournisseur se charge correctement en suivant les notifications d’événements [**msft \_ wmiprovider \_ OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) . Ces événements vous informent des échecs de chargement du fournisseur. Les autres classes de dépannage qui peuvent être utiles sont [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) et [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace). Pour plus d’informations sur les fournisseurs de dépannage, consultez [débogage des fournisseurs](debugging-providers.md) et [des classes de dépannage et de configuration du fournisseur](provider-configuration-and-troubleshooting-classes.md).
-   Si le fournisseur est un fournisseur d’instances ou de méthodes, veillez à tester chaque fonctionnalité de fournisseur une par une pour éviter toute confusion dans la logique de votre code.
-   Pour un fournisseur d’instance, créez une application cliente ou un script qui appelle chaque interface du fournisseur (énumération, obtenir, placer et supprimer). Même si le fournisseur n’est pas censé implémenter quoi que ce soit, il doit retourner un message « non pris en charge ». Vous pouvez trouver les valeurs de retour déjà définies dans les [codes de retour WMI](wmi-return-codes.md).
-   Pour vous assurer que le contexte de sécurité souhaité fonctionne comme prévu, appelez les opérations prises en charge par le fournisseur à partir d’un contexte de sécurité non administrateur. Le fournisseur doit prendre en charge l’emprunt d’identité. Si un utilisateur qui ne dispose pas des informations d’identification de sécurité appropriées tente de mettre à jour des données ou d’effectuer une opération qui exécute une méthode, votre fournisseur doit refuser l’accès avec le message d’erreur approprié.
-   Pour plus d’informations sur la sécurité du fournisseur, consultez [sécurisation de votre fournisseur](securing-your-provider.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hébergement et sécurité du fournisseur](provider-hosting-and-security.md)
</dt> <dt>

[Fourniture de données à WMI en écrivant un fournisseur](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Inscription d’un fournisseur](registering-a-provider.md)
</dt> <dt>

[Résolution des problèmes des applications clientes WMI](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> <dt>

[Obtention et fourniture de données sur une plateforme 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
