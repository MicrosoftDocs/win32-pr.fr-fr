---
title: Licences et IClassFactory2
description: Licences et IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9376d5187588ba14da434161309409bf1d189a8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216652"
---
# <a name="licensing-and-iclassfactory2"></a>Licences et IClassFactory2

L’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) sur un objet de classe fournit le mécanisme de création d’objet de base de com. À l’aide d' **IClassFactory**, un serveur peut contrôler la création d’objets sur une base de machines. L’implémentation de la méthode [**IClassFactory :: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) peut autoriser ou interdire la création d’objets en fonction de l’existence d’une licence d’ordinateur. Une licence d’ordinateur est une information distincte de l’application qui existe sur un ordinateur pour indiquer que le logiciel a été installé à partir d’une source valide, telle que les disques d’installation du fournisseur. Si la licence de l’ordinateur n’existe pas, le serveur peut autoriser la création de l’objet. La licence d’ordinateur empêche le piratage dans les cas où un utilisateur tente de copier le logiciel d’un ordinateur vers un autre, car les informations de licence ne sont pas copiées avec le logiciel et l’ordinateur qui reçoit la copie n’est pas concédé sous licence.

Toutefois, dans un logiciel de composants, les fournisseurs ont besoin d’un niveau de contrôle plus fin sur les licences. En plus du contrôle de licence d’ordinateur, un fournisseur doit autoriser certains clients à créer un objet composant tout en refusant la même fonctionnalité aux autres clients. Cela nécessite que l’application cliente obtienne une clé de licence du composant pendant que l’application cliente est toujours en cours de développement. L’application cliente utilise la clé de licence au moment de l’exécution pour créer des objets sur un ordinateur sans licence.

Par exemple, si un fournisseur fournit une bibliothèque de contrôles aux développeurs, le développeur qui achète la bibliothèque aura une licence d’ordinateur complète, ce qui permettra de créer les objets sur l’ordinateur de développement. Le développeur peut ensuite créer une application cliente sur l’ordinateur sous licence, en incorporant un ou plusieurs contrôles. Lorsque l’application cliente résultante est exécutée sur un autre ordinateur, les contrôles utilisés dans l’application cliente doivent être créés sur l’autre ordinateur, même si cet ordinateur ne possède pas de licence d’ordinateur pour les contrôles du fournisseur d’origine.

L’interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) fournit ce niveau de contrôle. Pour autoriser la gestion des licences basées sur les clés pour un composant donné, vous devez implémenter **IClassFactory2** sur l’objet de fabrique de classes pour ce composant. **IClassFactory2** est dérivée de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), donc en implémentant **IClassFactory2**, l’objet de fabrique de classes répond aux exigences de base de com.

Pour incorporer un composant sous licence dans votre application cliente, utilisez les méthodes suivantes dans [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2):

-   La méthode [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) remplit une structure [**LICINFO**](/windows/win32/api/ocidl/ns-ocidl-licinfo) avec des informations décrivant le comportement de la licence de la fabrique de classes. Par exemple, la fabrique de classe peut fournir des clés de licence pour la licence au moment de l’exécution si le membre **fRunTimeKeyAvail** a la **valeur true**.
-   La méthode [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) fournit une clé de licence pour le composant. Une licence d’ordinateur doit être disponible lorsque le client appelle cette méthode.
-   La méthode [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) crée une instance du composant sous licence si le paramètre de clé de licence (BSTRÂ bstrKey) est valide.

> [!Note]  
> Dans ses informations de type, un composant utilise l’attribut sous licence pour marquer la coclasse qui prend en charge la gestion des licences par le biais de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2).

 

Tout d’abord, vous avez besoin d’un outil de développement distinct qui est également un client du composant sous licence. L’objectif de cet outil est d’obtenir la clé de licence d’exécution et de l’enregistrer dans votre application cliente. Cet outil s’exécute uniquement sur un ordinateur qui possède une licence d’ordinateur pour le composant. L’outil appelle les méthodes [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) et [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) pour obtenir la clé de licence d’exécution, puis enregistre la clé de licence dans votre application cliente. Par exemple, l’outil de développement peut créer un fichier d’en-tête (. h) contenant la clé de licence BSTR, puis inclure ce fichier. h dans votre application cliente.

Pour instancier le composant dans votre application cliente, essayez d’abord d’instancier l’objet directement avec [**IClassFactory :: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Si **CreateInstance** parvient à fonctionner, le deuxième ordinateur est concédé sous licence pour le composant et les objets peuvent être créés à l’adresse. Si **CreateInstance** échoue avec la classe de code de retour \_ E \_ NOTLICENSED, la seule façon de créer l’objet consiste à passer la clé d’exécution à la méthode [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) . **CreateInstanceLic** vérifie la clé et crée l’objet si la clé est valide.

De cette façon, une application générée avec des composants (tels que des contrôles) peut s’exécuter sur un ordinateur qui n’a pas d’autre licence ; seule l’application cliente contenant la licence d’exécution est autorisée à créer les objets de composant en question.

L’interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) prend en charge la flexibilité des modèles de licence. Par exemple, l’implémenteur de serveur peut chiffrer les clés de licence dans le composant pour renforcer la sécurité. Les implémenteurs de serveur peuvent également activer ou désactiver des niveaux de fonctionnalités dans leurs objets en fournissant différentes clés de licence pour différentes fonctions. Par exemple, une clé peut autoriser un niveau de base de fonctionnalité, tandis qu’une autre offre des fonctionnalités de base et avancées, et ainsi de suite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Responsabilités du serveur COM](com-server-responsibilities.md)
</dt> </dl>

 

 