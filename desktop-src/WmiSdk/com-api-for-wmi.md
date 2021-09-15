---
description: Vous pouvez utiliser l’API COM (Component Object Model) WMI pour écrire des applications clientes de gestion ou créer un fournisseur WMI.
ms.assetid: 5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1
ms.tgt_platform: multiple
title: API COM pour WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb585badeeeaae947906bbfc783baf355863e05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403887"
---
# <a name="com-api-for-wmi"></a>API COM pour WMI

Vous pouvez utiliser l’API COM (Component Object Model) WMI pour écrire des applications clientes de gestion ou créer un [*fournisseur*](gloss-p.md)WMI. La référence de l’API COM fournit des informations pour les administrateurs système avancés, ainsi que pour les développeurs qui écrivent des applications clientes et fournisseur.

Pour plus d’informations sur l’écriture d’applications de gestion d’entreprise WMI, consultez [création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md). Pour plus d’informations sur l’écriture d’un fournisseur WMI, consultez [fourniture de données à WMI](providing-data-to-wmi.md).

> [!Note]  
> WMI prend en charge uniquement le développement C++ à l’aide de Microsoft Visual C++ systèmes de développement version 6,0 et versions ultérieures. Toutefois, vous pouvez également utiliser d’autres compilateurs, tels que ceux de Borland et Watcom.

 

Chacun des différents objets WMI hérite d’une interface qui est finalement héritée de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . COM détermine comment les implémenteurs d’objets, ou interfaces, gèrent des tâches telles que la gestion de la mémoire, la gestion des paramètres et le multithreading. En se conformant à COM, l’API COM pour WMI s’assure qu’elle prend en charge les fonctionnalités fournies par les interfaces de chaque objet WMI.

WMI est accessible via les interfaces COM spécifiques à WMI suivantes.



| Interface                                                                    | Description                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)                         | Énumérateur qui fonctionne avec les objets de type [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject). Elle est similaire aux énumérateurs COM standard, tels que [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).                                                                                                      |
| [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)                                         | Implémenté par Mofd.dll, cette interface fournit une interface COM qui est utilisée par le compilateur MOF et toutes les autres applications qui compilent des fichiers MOF.                                                                                                                                                       |
| [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)                           | Utilisé pour simplifier le processus de création d’appels asynchrones à partir d’un processus client.                                                                                                                                                                                                                           |
| [**IWbemBackupRestore**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbembackuprestore)                             | Sauvegarde et restaure le contenu de l’espace de stockage WMI.                                                                                                                                                                                                                                                  |
| [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                                   | Utilisé pour les appels [semi-synchrones](making-a-semisynchronous-call-with-c--.md) de l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Lors de ces appels, la méthode **IWbemServices** appelée est retournée immédiatement, avec un objet [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .                    |
| [**IWbemCausalityAnalysis**](iwbemcausalityaccess.md)                       | Effectue le suivi des demandes enfants générées à partir d’une demande parente.                                                                                                                                                                                                                                            |
| [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)                                 | Contient et manipule les définitions de classe et les instances d’objet de classe. Les développeurs n’ont pas besoin d’implémenter cette interface ; WMI fournit son implémentation.                                                                                                                                                 |
| [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)                   | Utilisé par le code client pour ajouter ou supprimer des énumérateurs, des objets et des actualisateurs imbriqués dans un actualisateur.                                                                                                                                                                                                         |
| [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)                                         | éventuellement utilisé pour communiquer des informations de contexte supplémentaires aux fournisseurs lors de la soumission d’appels [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) à la gestion des Windows.                                                                                                                                             |
| [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider) | Inscrit des fournisseurs découplés avec WMI.                                                                                                                                                                                                                                                                    |
| [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar)                   | Associe des fournisseurs découplés à WMI. Cette interface permet à un fournisseur hébergé par un processus de définir la durée de vie de l’interopérabilité de l’interface et de coexister avec d’autres fournisseurs.                                                                                                                        |
| [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)             | Fournit l’interface principale pour un fournisseur de consommateur d’événements. Grâce à cette interface et à la méthode [**FindConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer) , un fournisseur de consommateur d’événements peut indiquer les consommateurs d’événements qui doivent recevoir un événement donné.                                          |
| [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)                             | Utilisé pour initier la communication avec un fournisseur d’événements.                                                                                                                                                                                                                                                     |
| [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)           | Éventuellement implémenté par des fournisseurs d’événements qui souhaitent savoir quels types de filtres de requête d’événement sont actuellement actifs pour optimiser les performances.                                                                                                                                                                 |
| [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity)             | Éventuellement implémenté par des fournisseurs d’événements qui souhaitent restreindre l’accès des consommateurs à leur événement.                                                                                                                                                                                                             |
| [**IWbemEventSink**](iwbemeventsink.md)                                     | Lance la communication avec un fournisseur d’événements à l’aide d’un ensemble restreint de requêtes. Cette interface étend [**IWbemObjectSink**](iwbemobjectsink.md), en fournissant de nouvelles méthodes pour la sécurité et les performances.                                                                                          |
| [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)                           | Permet aux fournisseurs de fournir des objets et des énumérateurs actualisables.                                                                                                                                                                                                                                           |
| [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum)                                   | Utilisé dans les opérations d’actualisation pour fournir un accès rapide aux énumérations des objets d’instance.                                                                                                                                                                                                                  |
| [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)                                         | Obtient le pointeur d’espace de noms initial de l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour WMI sur un ordinateur hôte spécifique.                                                                                                                                                                         |
| [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)                               | Fournit l’accès aux méthodes et propriétés d’un objet. Un objet [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) est un conteneur pour une instance mise à jour par un [*actualisateur*](gloss-r.md).                                                                                           |
| [**IWbemObjectSink**](iwbemobjectsink.md)                                   | Utilisé pour recevoir les résultats de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) et certains types de notifications d’événements.                                                                                                                                                                                       |
| [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)                             | Utilisé pour convertir des instances [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) vers et depuis des formats de texte différents.                                                                                                                                                                                               |
| [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)                       | Prend en charge la récupération et la mise à jour de propriétés individuelles dans une instance d’une classe WMI.                                                                                                                                                                                                                      |
| [**IWbemProviderIdentity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemprovideridentity)                       | Implémenté par un fournisseur d’événements si le fournisseur s’inscrit lui-même à l’aide de plusieurs **noms** (plusieurs instances de [**\_ \_ Win32Provider**](--win32provider.md)) avec la même valeur de [CLSID](../com/clsid.md) . La classe fournit un mécanisme permettant de distinguer le fournisseur nommé qui doit être utilisé. |
| [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)                               | Utilisé pour initialiser les fournisseurs.                                                                                                                                                                                                                                                                              |
| [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)                       | Implémenté par WMI et appelé par les fournisseurs pour signaler l’état de l’initialisation.                                                                                                                                                                                                                                |
| [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)                               | Agit comme un conteneur pour le jeu entier de qualificateurs nommés pour une propriété unique ou un objet entier (une classe ou une instance).                                                                                                                                                                                   |
| [**IWbemQuery**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbemquery)                                             | Fournit un point d’entrée par le biais duquel une requête [*langage de requêtes WMI (WQL)*](gloss-w.md) (WQL) peut être analysée.                                                                                                                                                                        |
| [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)                                     | Fournit un point d’entrée par le biais duquel des objets actualisables tels que des énumérateurs ou des objets actualisateurs peuvent être actualisés.                                                                                                                                                                                      |
| [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                       | Utilisé par les clients et les fournisseurs pour accéder aux services WMI. L’interface est implémentée uniquement par WMI et est l’interface WMI principale.                                                                                                                                                                           |
| [**IWbemStatusCodeText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemstatuscodetext)                           | Extrait les descriptions de chaîne de texte des codes d’erreur ou le nom du sous-système où l’erreur s’est produite.                                                                                                                                                                                                    |
| [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)                     | Implémenté par tous les consommateurs d’événements logiques. Il s’agit d’une interface de récepteur simple qui accepte la remise d’objets d’événement.                                                                                                                                                                                          |



 

> [!Note]  
> La plupart des fonctions COM WMI retournent des codes d’erreur numériques documentés en tant que constantes nommées. Ces constantes sont définies dans Wbemcli. h dans le \\ dossier include WMI SDK. Pour plus d’informations, consultez [codes de retour WMI](wmi-return-codes.md).

 

Pour plus d’informations sur les rubriques suivantes relatives à la programmation COM, consultez [développement de composants]( /previous-versions//ee663263(v=vs.85)):

-   Interfaces et conception d’objets.
-   Implémentation de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   Gestion de la mémoire
-   Gestion du décompte de références.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence WMI](wmi-reference.md)
</dt> </dl>

 

 
