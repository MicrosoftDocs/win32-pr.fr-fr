---
title: Vue d’ensemble technique COM
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: 'En savoir plus sur : vue d’ensemble technique de COM'
keywords:
- COM présentation technique com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5dc95ffae5166d86cd8110cab1a6b90e6ffa5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110571"
---
# <a name="com-technical-overview"></a>Vue d’ensemble technique COM

Cette rubrique fournit une vue d’ensemble du modèle COM (Component Object Model) Microsoft :

-   [Introduction à COM](#introduction-to-com)
-   [Objets et interfaces](#objects-and-interfaces)
-   [Implémentation de l’interface](#interface-implementation)
-   [Interface IUnknown](#the-iunknown-interface)
-   [Modèle client/serveur](#the-clientserver-model)
-   [Gestionnaire de contrôle des services](#service-control-manager)
-   [Réutilisabilité](#reusability)
-   [Objets de stockage et de flux](#storage-and-stream-objects)
-   [Transfert de données](#data-transfer)
-   [Communication à distance](#remoting)
-   [Sécurité](#security)
-   [Rubriques connexes](#related-topics)

## <a name="introduction-to-com"></a>Introduction à COM

Le modèle COM (Component Object Model) Microsoft définit une norme d’interopérabilité binaire pour créer des bibliothèques logicielles réutilisables qui interagissent au moment de l’exécution. Vous pouvez utiliser des bibliothèques COM sans avoir besoin de les compiler dans votre application. COM est la base d’un certain nombre de produits et de technologies Microsoft, tels que Windows Media Player et Windows Server.

COM définit une norme binaire qui s’applique à de nombreux systèmes d’exploitation et plates-formes matérielles. Pour l’informatique en réseau, COM définit un protocole et un format de câble standard pour l’interaction entre les objets qui s’exécutent sur différentes plateformes matérielles. COM est indépendant du langage d’implémentation, ce qui signifie que vous pouvez créer des bibliothèques COM à l’aide de différents langages de programmation, tels que C++ et ceux du .NET Framework.

La spécification COM fournit tous les concepts fondamentaux qui permettent la réutilisation de logiciels interplateformes :

-   Norme binaire pour les appels de fonction entre les composants.
-   Provision pour les regroupements fortement typés de fonctions en interfaces.
-   Interface de base qui fournit le polymorphisme, la découverte des fonctionnalités et le suivi de la durée de vie des objets.
-   Mécanisme qui identifie de façon unique les composants et leurs interfaces.
-   Chargeur de composant qui crée des instances de composant à partir d’un déploiement.

COM a un certain nombre de parties qui fonctionnent ensemble pour permettre la création d’applications créées à partir de composants réutilisables :

-   *Système hôte* qui fournit un environnement d’exécution conforme à la spécification com.
-   Les *interfaces* qui définissent les contrats de fonctionnalités et les *composants* qui implémentent les interfaces.
-   Les *serveurs* qui fournissent des composants au système, ainsi que les *clients* qui utilisent les fonctionnalités fournies par les composants.
-   *Registre* qui effectue le suivi des emplacements où les composants sont déployés sur des hôtes locaux et distants.
-   *Gestionnaire de contrôle des services* qui localise les composants sur les hôtes locaux et distants et connecte les serveurs aux clients.
-   Protocole de *stockage structuré* qui définit comment parcourir le contenu des fichiers sur le système de fichiers de l’hôte.

L’activation de la réutilisation de code sur les hôtes et les plateformes est essentielle à COM. Une implémentation d’interface réutilisable est nommée un *composant*, un *objet de composant* ou un *objet com*. Un composant implémente une ou plusieurs interfaces COM.

Vous définissez une bibliothèque COM personnalisée en concevant les interfaces implémentées par votre bibliothèque. Les consommateurs de votre bibliothèque peuvent découvrir et utiliser ses fonctionnalités sans aucune connaissance du déploiement et des détails de l’implémentation de votre bibliothèque.

## <a name="objects-and-interfaces"></a>Objets et interfaces

Un objet COM expose ses fonctionnalités par le biais d’une *interface*, qui est une collection de fonctions membres. Une interface COM définit le comportement et les responsabilités attendus d’un composant, et spécifie un contrat fortement typé qui fournit un petit ensemble d’opérations connexes. Toutes les communications entre les composants COM se produisent par le biais d’interfaces, et tous les services offerts par un composant sont exposés via son interface. Un appelant peut accéder uniquement aux fonctions membres de l’interface. L’état interne n’est pas disponible pour un appelant, sauf s’il est exposé dans l’interface.

Les interfaces sont fortement typées. Chaque interface a son propre identificateur d’interface unique, appelé IID, ce qui élimine les collisions pouvant se produire avec des noms explicites. L’IID est un identificateur global unique (GUID), qui est identique à l’identificateur unique universel (UUID) défini par l’environnement de calcul distribué OSF (Open Software Foundation). Lorsque vous créez une nouvelle interface, vous devez créer un nouvel identificateur pour cette interface. Quand un appelant utilise une interface, il doit utiliser l’identificateur unique. Cette identification explicite améliore la robustesse en éliminant les conflits de noms qui entraîneraient un échec au moment de l’exécution.

Lorsque vous définissez une nouvelle interface, vous pouvez créer une définition d’interface à l’aide du langage IDL (Interface Definition Language). À partir de cette définition d’interface, le compilateur IDL Microsoft génère des fichiers d’en-tête pour une utilisation par les applications à l’aide de l’interface et du code source pour gérer les appels de procédure distante. L’IDL fourni par Microsoft est basé sur des extensions simples de l’IDL DCE, une norme du secteur pour l’informatique distribuée basée sur les appels de procédure distante (RPC). IDL est un outil pour la commodité du concepteur d’interface et n’est pas central pour l’interopérabilité COM. Avec IDL, vous n’avez pas besoin de créer manuellement des fichiers d’en-tête pour chaque environnement de programmation. Pour plus d’informations, consultez [définition des interfaces com](defining-com-interfaces.md).

L’héritage est utilisé avec modération dans les interfaces COM. COM prend en charge l’héritage d’interface uniquement pour réutiliser un contrat associé à une interface de base. COM ne prend pas en charge l’héritage sélectif ; par conséquent, si une interface hérite d’une autre, elle comprend toutes les fonctions définies par l’interface de base. En outre, les interfaces utilisent uniquement l’héritage unique, au lieu de plusieurs héritages, pour obtenir des fonctions à partir d’une interface de base.

## <a name="interface-implementation"></a>Implémentation de l’interface

Vous ne pouvez pas créer une instance d’une interface COM seule. Au lieu de cela, vous créez une instance d’une classe qui implémente l’interface. En C++, une interface COM est modélisée en tant que *classe de base abstraite*, ce qui signifie que l’interface est une classe C++ qui contient uniquement des fonctions membres virtuelles pures. Une bibliothèque C++ implémente des objets COM en héritant des signatures de fonction membre d’une ou plusieurs interfaces, en substituant chaque fonction membre et en fournissant une implémentation pour chaque fonction.

Vous pouvez utiliser n’importe quel langage de programmation qui prend en charge le concept de pointeurs de fonction pour implémenter une interface COM. Par exemple, en C, une interface est une structure contenant un pointeur vers une table de pointeurs de fonction, un pour chaque méthode dans l’interface.

Lorsque vous implémentez une interface, votre classe doit fournir une implémentation pour chaque fonction dans l’interface. Si la classe n’a pas de travail à effectuer dans une fonction d’interface, l’implémentation peut être une instruction return unique.

Une classe COM est identifiée à l’aide d’un ID de classe 128 bits unique (CLSID) qui associe une classe à un déploiement particulier dans le système de fichiers, qui pour Windows est une DLL ou un EXE. Un CLSID est un GUID, ce qui signifie qu’aucune autre classe n’a le même CLSID. L’utilisation d’identificateurs de classe uniques empêche les collisions de noms entre les classes. Par exemple, deux fournisseurs différents peuvent écrire une classe nommée CStack, mais les deux classes ont un CLSID unique, de sorte que toute possibilité de collision est évitée.

Vous obtenez un nouveau CLSID à l’aide de la fonction [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) ou à l’aide d’un outil de création com, tel que Visual Studio, qui appelle cette fonction en interne.

## <a name="the-iunknown-interface"></a>Interface IUnknown

Toutes les interfaces COM héritent de l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . L’interface **IUnknown** contient les opérations com fondamentales pour la gestion de la durée de vie du polymorphisme et des instances. L’interface **IUnknown** a trois fonctions membres, nommées [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Tous les objets COM sont requis pour implémenter l’interface **IUnknown** .

La fonction membre [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) fournit le polymorphisme pour com. Appelez **QueryInterface** pour déterminer au moment de l’exécution si un objet com prend en charge une interface particulière. L’objet COM retourne un pointeur d’interface dans le `ppvObject` paramètre s’il implémente l’interface demandée ; sinon, il retourne `NULL` . La fonction membre **QueryInterface** active la navigation parmi toutes les interfaces prises en charge par un objet com.

La durée de vie d’une instance d’objet COM est contrôlée par son *décompte de références*. Les [](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) fonctions membres IUnknown [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) contrôlent le nombre. **AddRef** incrémente le nombre et la **libération** décrémente le nombre. Lorsque le décompte de références atteint zéro, la fonction membre **Release** peut libérer l’instance, car aucun appelant ne l’utilise.

## <a name="the-clientserver-model"></a>Modèle client/serveur

Une classe COM implémente un certain nombre d’interfaces COM. L’implémentation se compose de fichiers binaires qui s’exécutent lorsqu’un appelant interagit avec une instance de la classe COM. COM permet l’utilisation d’une classe dans différentes applications, y compris les applications écrites sans connaissance d’une classe particulière. Sur une plate-forme Windows, les classes existent dans une bibliothèque de liens dynamiques (DLL) ou dans une autre application (EXE).

Sur son système hôte, COM gère une base de données d’inscription de tous les CLSID pour les objets COM installés sur le système. La base de données d’inscription est un mappage entre chaque CLSID et l’emplacement de la DLL ou de l’EXE qui héberge la classe correspondante. COM interroge cette base de données chaque fois qu’un appelant souhaite créer une instance d’une classe COM. L’appelant doit connaître uniquement le CLSID pour demander une nouvelle instance de la classe.

L’interaction entre un objet COM et ses appelants est modélisée en tant que relation client/serveur. Le client est l’appelant qui demande un objet COM du système, et le serveur est le module qui héberge les objets COM qui fournit des services aux clients.

Un client COM est un appelant qui passe un CLSID au système pour demander une instance d’un objet COM. La façon la plus simple de créer une instance consiste à appeler la fonction COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

La fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) crée une instance du CLSID spécifié et retourne un pointeur d’interface du type demandé par le client. Le client est responsable de la gestion de la durée de vie de l’instance en appelant sa fonction [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) lorsque le client a fini de l’utiliser. Pour créer plusieurs objets basés sur un seul CLSID, appelez la fonction [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) . Pour vous connecter à un objet déjà créé et en cours d’exécution, appelez la fonction [**GetActiveObject**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject) .

Un serveur COM fournit une implémentation COM au système. Un serveur associe un CLSID à une classe COM, héberge l’implémentation de la classe, implémente une fabrique de classes pour créer des instances de la classe et permet de décharger le serveur.

> [!Note]  
> Un serveur COM n’est pas le même que l’objet COM qu’il fournit au système.

 

Pour permettre la création d’un objet COM, un serveur COM doit fournir une implémentation de l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Les clients peuvent appeler la méthode [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) pour demander une nouvelle instance d’un objet com, mais ces demandes sont généralement encapsulées dans la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

Vous pouvez déployer un serveur COM en tant que bibliothèque partagée qui est chargée dans le processus du client au moment de l’exécution (DLL sur les plateformes Windows) ou en tant que module exécutable (EXE sur les plateformes Windows). Pour plus d’informations, consultez [inscription d’applications com](registering-com-applications.md).

## <a name="service-control-manager"></a>Gestionnaire de contrôle des services

Le gestionnaire de contrôle des services (SCM) gère la demande du client pour une instance d’un objet COM. La liste suivante présente la séquence des événements :

-   Un client demande un pointeur d’interface à un objet COM à partir de la bibliothèque COM en appelant une fonction telle que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec le CLSID de l’objet com.
-   La bibliothèque COM interroge le SCM pour trouver le serveur qui correspond au CLSID demandé.
-   Le SCM localise le serveur et demande la création de l’objet COM à partir de la fabrique de classes fournie par le serveur.
-   En cas de réussite, la bibliothèque COM retourne un pointeur d’interface vers le client.

Une fois que le système COM a connecté un objet serveur à un client, le client et l’objet communiquent directement. Il n’y a aucune surcharge supplémentaire due à l’appel par le biais d’une exécution intermédiaire.

Lorsque vous inscrivez un serveur COM auprès du système hôte, vous pouvez spécifier différentes méthodes d’activation du serveur. La liste suivante présente les trois façons dont le SCM peut activer un serveur COM :

-   In-process : le SCM retourne le chemin d’accès de fichier de la DLL qui contient l’implémentation du serveur d’objets. La bibliothèque COM charge la DLL et l’interroge pour son pointeur d’interface de fabrique de classes.
-   Local : le SCM démarre l’exécutable local qui inscrit une fabrique de classe au démarrage, et son pointeur d’interface est disponible pour le système et les clients.
-   Distant : le SCM local acquiert un pointeur d’interface de fabrique de classes à partir du SCM qui s’exécute sur un ordinateur distant.

Lorsqu’un client demande un objet COM, la bibliothèque COM contacte le SCM sur l’hôte local. Le SCM localise le serveur COM approprié, qui peut être local ou distant, et le serveur retourne un pointeur d’interface vers la fabrique de classe du serveur. Lorsque la fabrique de classe est disponible, la bibliothèque COM ou le client peut utiliser la fabrique de classe pour créer l’objet demandé. Pour plus d’informations, consultez [Implementing IClassFactory](implementing-iclassfactory.md).

## <a name="reusability"></a>Possibilité de réutilisation

COM prend en charge la *réutilisation de la boîte noire*, ce qui signifie que les détails d’implémentation d’un composant réutilisable ne sont pas exposés aux clients. Pour permettre la réutilisation de la boîte noire, COM prend en charge deux mécanismes par lesquels un objet peut réutiliser un autre. Les deux formes de réutilisation sont des *imbrications* et des *agrégations* nommées. Par Convention, l’objet qui est réutilisé est nommé l' *objet interne* et l’objet qui utilise l’objet interne est nommé l' *objet externe*.

Dans la relation contenant-contenu, l’objet externe se comporte comme un client de l’objet interne. L’objet externe est un conteneur logique pour l’objet interne et, lorsque l’objet externe utilise les services de l’objet interne, l’objet externe délègue l’implémentation aux interfaces de l’objet interne. Cela signifie que l’objet externe est implémenté en termes de services de l’objet interne. L’objet externe peut ne pas prendre en charge les mêmes interfaces que l’objet interne, et l’objet externe peut utiliser l’interface d’un objet interne pour faciliter l’implémentation des parties d’une interface différente sur l’objet externe.

Dans l’agrégation, l’objet externe expose les interfaces de l’objet interne comme si elles étaient implémentées sur l’objet externe. Cela est utile lorsque l’objet externe délègue toujours chaque appel sur l’une de ses interfaces à la même interface de l’objet interne. L’agrégation est une pratique qui permet à l’objet externe d’éviter une surcharge d’implémentation supplémentaire.

Pour plus d’informations, consultez [réutilisation des objets](reusing-objects.md).

## <a name="storage-and-stream-objects"></a>Objets de stockage et de flux

Les objets COM enregistrent l’État dans un fichier à l’aide du *stockage structuré*, qui est une forme de stockage persistant qui permet la navigation dans le contenu d’un fichier à l’aide de la sémantique du système de fichiers. Le traitement du contenu d’un fichier de cette manière active des fonctionnalités telles que l’accès incrémentiel, les transactions et le partage entre les processus.

La spécification de stockage persistant COM fournit deux types d’éléments de stockage : les objets de stockage et les objets de flux. Ces objets sont implémentés par la bibliothèque COM, et les applications utilisateur implémentent rarement ces éléments de stockage. Les objets de stockage implémentent l’interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , et les objets de flux implémentent l’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .

Un objet de flux contient des données et est conceptuellement similaire à un fichier unique dans un système de fichiers. Chaque flux dispose de droits d’accès et d’un seul pointeur de recherche. À l’aide de l’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , vous pouvez lire, écrire, Rechercher et exécuter d’autres opérations sur les données sous-jacentes du flux. Un flux est nommé à l’aide d’une chaîne de texte. Il peut contenir n’importe quelle structure interne, car il s’agit d’un flux plat d’octets. En outre, les fonctions de l’interface **IStream** sont similaires aux fonctions standard basées sur les handles de fichiers, telles que celles de la bibliothèque Runtime C ANSI.

Un objet de stockage est conceptuellement similaire à un répertoire dans un système de fichiers. Chaque stockage peut contenir un nombre quelconque d’objets de sous-stockage et un nombre quelconque de flux. Chaque stockage dispose de ses propres droits d’accès. À l’aide de l’interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , vous pouvez effectuer des opérations telles que l’énumération, le déplacement, la copie, le changement de nom, la création et la suppression d’éléments. Un objet de stockage ne stocke pas les données définies par l’application, mais stocke implicitement les noms des éléments (stockages et flux) qu’il contient.

Les objets de stockage et de flux sont partageables entre les processus lorsqu’ils sont implémentés conformément à la spécification COM sur une plateforme hôte. Cela permet aux objets qui exécutent in-process ou out-of-process d’avoir un accès incrémentiel équivalent à leur stockage de fichiers. Étant donné que COM est chargé séparément dans chaque processus, il utilise des mécanismes de mémoire partagée pris en charge par le système d’exploitation pour communiquer l’état des éléments ouverts et leurs modes d’accès entre les processus.

Chaque objet de stockage et de flux d’un fichier structuré a un nom pour l’identifier. Le nom est une chaîne qui suit une convention particulière. Pour plus d’informations, consultez [conventions d’affectation de noms](/windows/desktop/Stg/storage-object-naming-conventions)pour les objets de stockage. Le nom est passé aux fonctions [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) pour spécifier l’élément dans le stockage sur lequel opérer. Les noms des objets de stockage racine sont les mêmes que les noms de fichiers dans le système de fichiers sous-jacent, et ces noms doivent respecter les conventions et restrictions du système de fichiers. Chaînes passées aux fonctions liées au stockage, dont les fichiers de noms sont transmis au système de fichiers sans interprétation ou modification.

Les noms des éléments contenus dans les objets de stockage sont gérés par l’implémentation de l’objet de stockage en question. Toutes les implémentations des objets de stockage doivent prendre en charge les noms d’éléments de 32 caractères, et certaines implémentations peuvent prendre en charge des noms plus longs. Les noms sont stockés avec la casse conservée, mais ils sont comparés comme ne respectant pas la casse. Les applications qui définissent les noms des éléments de stockage doivent choisir des noms qui fonctionnent dans les deux cas.

Vous accédez à chaque élément d’un fichier de stockage structuré en utilisant des fonctions et des interfaces implémentées par COM. Cela signifie que d’autres applications peuvent parcourir le fichier en naviguant avec les fonctions d’interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) qui fournissent des services de type annuaire. En outre, d’autres applications peuvent utiliser les données du fichier, sans avoir à exécuter l’application qui a écrit le fichier. Lorsqu’une application COM accède aux fichiers de stockage structurés d’une autre application, les droits d’accès Windows standard s’appliquent et l’application doit disposer de privilèges suffisants.

Un objet COM peut lire et écrire lui-même dans un stockage persistant. Un client interroge l’une des interfaces relatives à la persistance sur l’objet COM, en fonction du contexte de l’opération. Les objets COM peuvent implémenter n’importe quelle combinaison des interfaces suivantes :

-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage): l’objet com lit et écrit son état persistant dans un objet de stockage. Le client fournit l’objet avec un pointeur [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) via cette interface. Il s’agit de la seule interface de persistance qui comprend la sémantique pour l’accès incrémentiel.
-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream): l’objet com lit et écrit son état persistant dans un objet de flux. Le client fournit l’objet avec un pointeur [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) via cette interface.
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile): l’objet com lit et écrit son état persistant directement dans un fichier sur le système sous-jacent. Cette interface n’implique pas [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , sauf si le fichier sous-jacent est accessible par le biais de ces interfaces, mais l’interface **IPersistFile** n’a aucune sémantique pour les stockages et les flux. Le client fournit l’objet avec un nom de fichier et appelle les fonctions [**Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) ou [**Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load) .

## <a name="data-transfer"></a>Transfert de données

Le stockage structuré fournit la base pour l’échange de données entre les processus et les objets COM, qui est nommé *transfert de données uniforme*. Avant l’implémentation de COM dans OLE 2, le transfert de données sur Windows était spécifié par les *protocoles de transfert*, tels que le presse-papiers et les protocoles de glisser-déplacer. Chaque protocole de transfert avait son propre ensemble de fonctions qui délimitent le protocole à la requête, et du code spécifique était nécessaire pour gérer chaque protocole et procédure d’échange. Le transfert de données uniforme représente tous les transferts de données à l’aide de l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , qui sépare les opérations courantes d’échange de données du protocole de transfert.

L’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) encapsule les opérations d’extraction et de définition standard sur les données, les requêtes et les énumérations, et les notifications qui détectent le moment où les données sont modifiées dans un objet. Le transfert de données uniforme permet une description détaillée des formats de données, ainsi que l’utilisation de différents supports de stockage pour le transfert de données.

Lors du transfert de données uniforme, tous les protocoles échangent un pointeur vers une interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Le serveur est la source des données et implémente un objet de données qui est utilisable dans tout protocole d’échange de données. Le client consomme les données et demande des données à partir d’un objet de données lorsqu’il reçoit un pointeur **IDataObject** de n’importe quel protocole. Une fois l’échange de pointeur effectué, les deux côtés gèrent l’échange de données de manière uniforme, via l’interface **IDataObject** .

COM définit deux structures de données qui permettent le transfert de données uniforme. La structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) représente un format de presse-papiers généralisé, et la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) représente le support de transfert sous la forme d’un handle de mémoire.

Le client crée une structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) pour indiquer le type de données qu’il demande à partir d’une source de données, et il est utilisé par la source de données pour décrire les formats qu’il fournit. Le client interroge une source de données à la recherche de ses formats disponibles en demandant son interface [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . Pour plus d’informations, consultez [la structure FORMATETC](the-formatetc-structure.md).

Le client crée une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) et la passe à la méthode [**GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) , et l’objet de données retourne les données dans la structure **STGMEDIUM** fournie.

La structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permet aux clients et aux sources de données de choisir le support Exchange le plus efficace. Par exemple, si les données à échanger sont très volumineuses, la source de données peut indiquer un support sur disque comme format préféré, au lieu de la mémoire principale. Cette flexibilité permet d’échanger efficacement des données qui peuvent être aussi rapides que le passage d’un pointeur vers une [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) ou un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Pour plus d’informations, consultez [la structure STGMEDIUM](the-stgmedium-structure.md).

Un client d’une source de données peut nécessiter une notification lorsque les données sont modifiées. COM gère les notifications de modification de données à l’aide d’un objet de *récepteur* de notifications, qui implémente l’interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) . L’objet de récepteur de notifications et l’interface **IAdviseSink** sont implémentés par le client, qui passe un pointeur **IAdviseSink** à la source de données. Lorsque la source de données détecte une modification apportée aux données sous-jacentes, elle appelle une méthode **IAdviseSink** pour notifier le client. Pour plus d’informations, consultez [notification de données](data-notification.md).

## <a name="remoting"></a>Communication à distance

COM active le calcul à distance et distribué. La *communication à distance* de l’interface permet à une fonction membre de retourner un pointeur d’interface vers un objet com qui se trouve dans un processus différent ou sur un ordinateur hôte différent. L’infrastructure qui effectue la communication à distance de l’interface est transparente pour le client et le serveur d’objets. Ni le client ni le serveur n’ont besoin des détails de déploiement d’un autre pour communiquer via une interface distante. Un client appelle des fonctions membres sur la même interface pour communiquer avec un objet COM qui est in-process, out-of-process sur l’hôte local ou sur un ordinateur distant. Les appels locaux et distants sur la même interface ne peuvent pas être différenciés par le client.

Pour communiquer avec un objet COM, un client appelle toujours une implémentation in-process. Si l’objet COM est in-process, l’appel est direct. Si l’objet COM est hors processus ou distant, COM fournit une implémentation de *proxy* qui transfère l’appel à l’objet à l’aide du protocole d’appel de procédure distante (RPC).

Un objet COM reçoit toujours les appels d’un client par le biais d’une implémentation in-process. Si l’appelant est in-process, l’appel est direct. Si l’appelant est hors processus ou distant, COM fournit une implémentation de *stub* qui reçoit l’appel de procédure distante du proxy dans le processus client.

Le *marshaling* est la procédure permettant d’empaqueter la pile des appels pour la transmission du proxy au stub. Le *démarshaling* est le désassemblage qui se produit à la fin de la réception. Les valeurs de retour sont marshalées et démarshalées du stub vers le proxy. Ce type de communication est également appelé envoi d’un appel *sur le réseau*.

Chaque type de données est associé à des règles de marshaling. Les pointeurs d’interface ont également un protocole de marshaling, qui est encapsulé dans la fonction [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) . Dans la plupart des cas, le *marshaling d’interface standard*, fourni par le système, est suffisant, mais un objet com peut éventuellement implémenter un *marshaling d’interface personnalisé* pour contrôler la création de proxys d’objets distants à lui-même. Pour plus d’informations, consultez [communication entre les objets](inter-object-communication.md).

## <a name="security"></a>Sécurité

COM fournit deux formes de sécurité des applications. L’une est la *sécurité d’activation*, qui spécifie la façon dont les nouveaux objets sont créés, la façon dont les clients se connectent aux objets nouveaux et existants, ainsi que la façon dont certains services publics, tels que la table de classes et la table d’objets en cours d’exécution, sont sécurisés. L’autre est *appeler Security*, qui spécifie comment la sécurité opère dans une connexion établie entre un client et un objet com.

La sécurité d’activation est appliquée automatiquement par le gestionnaire de contrôle des services (SCM). Lorsque le SCM reçoit une demande de récupération d’un objet COM, il vérifie la demande par rapport aux informations de sécurité stockées dans le registre.

Les implémentations SCM offrent généralement une configuration basée sur le registre pour l’administration des classes déployées et pour des comptes d’utilisateur spécifiques sur l’ordinateur hôte. Pour plus d’informations, consultez [sécurité de l’activation](activation-security.md).

La sécurité de l’appel est appliquée automatiquement ou est appliquée par l’application. Si l’application fournit des informations d’installation, COM effectue les vérifications nécessaires pour sécuriser l’application.

Le mécanisme automatique vérifie la sécurité pour le processus, mais pas pour les objets ou méthodes individuels. Si une application nécessite une sécurité plus précise, COM fournit des fonctions que les applications peuvent utiliser pour effectuer leur propre vérification de sécurité.

Les mécanismes automatiques et personnalisés peuvent être utilisés ensemble, de sorte qu’une application peut demander à COM de procéder à la vérification de la sécurité automatique, puis de l’exécuter.

Les services de sécurité des appels COM sont répartis dans les catégories suivantes :

-   Fonctions générales qui sont appelées par les clients et les serveurs, ce qui permet au mécanisme de sécurité automatique d’être inscrit et d’inscrire les services d’authentification automatique. Les API de sécurité d’appel générales sont les fonctions [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .
-   Interfaces sur les proxys clients, qui permettent au client de contrôler la sécurité sur les appels à des interfaces individuelles. L’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) et les fonctions [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)et [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) fournissent la sécurité de l’appel sur un objet distant.
-   Les fonctions côté serveur et les interfaces de contexte d’appel, qui permettent au serveur de récupérer les informations de sécurité relatives à un appel et d’emprunter l’identité de l’appelant. L’interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) et les fonctions [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)et [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself) fournissent la sécurité de l’appel côté serveur.

Souvent, le client interroge l’objet COM pour l’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) , qui est implémentée localement par la couche de communication à distance. Le client utilise cette interface pour contrôler la sécurité des proxies d’interface individuels sur l’objet COM avant d’effectuer un appel sur l’une des interfaces.

Lorsqu’un appel arrive sur le serveur, le serveur peut appeler la fonction [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) pour récupérer une interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) , ce qui permet au serveur de vérifier l’authentification du client et d’emprunter l’identité du client, si nécessaire. L’objet **IServerSecurity** est valide pour la durée de l’appel.

Appelez la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour initialiser la couche de sécurité et définir les valeurs spécifiées comme valeur par défaut de sécurité. Si un processus n’appelle pas **CoInitializeSecurity**, com l’appelle automatiquement la première fois qu’une interface est marshalée ou démarshalée, en inscrivant la sécurité par défaut du système. La fonction **CoInitializeSecurity** permet au client d’établir la sécurité de l’appel par défaut pour le processus, ce qui évite l’utilisation de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) sur des proxies individuels. La fonction **CoInitializeSecurity** permet à un serveur d’inscrire des services d’authentification automatique pour le processus. Pour plus d’informations, consultez [Setting Process-Wide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients et serveurs COM](com-clients-and-servers.md)
</dt> <dt>

[Définition d’interfaces COM](defining-com-interfaces.md)
</dt> <dt>

[Inscription des applications COM](registering-com-applications.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 
