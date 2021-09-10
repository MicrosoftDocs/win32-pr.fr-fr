---
title: Clients et serveurs COM
description: L’un des aspects essentiels de COM est la façon dont les clients et les serveurs interagissent.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363303"
---
# <a name="com-clients-and-servers"></a>Clients et serveurs COM

L’un des aspects essentiels de COM est la façon dont les clients et les serveurs interagissent. Un *client com* est le code ou l’objet qui obtient un pointeur vers un serveur com et utilise ses services en appelant les méthodes de ses interfaces. Un *serveur com* est un objet qui fournit des services aux clients. ces services se présentent sous la forme d’implémentations d’interface COM qui peuvent être appelées par n’importe quel client capable d’obtenir un pointeur vers l’une des interfaces sur l’objet serveur.

Il existe deux principaux types de serveurs : *in-process* et *out-of-process*. Les serveurs in-process sont implémentés dans une bibliothèque liée dynamique (DLL) et les serveurs hors processus sont implémentés dans un fichier exécutable (EXE). Les serveurs hors processus peuvent résider sur l’ordinateur local ou sur un ordinateur distant. En outre, COM fournit un mécanisme qui permet à un serveur in-process (une DLL) de s’exécuter dans un processus EXE de substitution pour tirer parti de la possibilité d’exécuter le processus sur un ordinateur distant. Pour plus d’informations, consultez [substituts de dll](dll-surrogates.md).

Les constructions et le modèle de programmation COM ont été étendus pour que les clients et les serveurs COM puissent travailler ensemble sur le réseau, et pas seulement au sein d’un ordinateur donné. Cela permet aux applications existantes d’interagir avec de nouvelles applications et entre elles sur des réseaux avec une administration correcte, et de nouvelles applications peuvent être écrites pour tirer parti des fonctionnalités de mise en réseau.

Les applications clientes COM n’ont pas besoin de savoir comment les objets serveur sont empaquetés, qu’ils soient empaquetés en tant qu’objets in-process (dans des dll) ou en tant qu’objets locaux ou distants (dans les fichiers exe). Le modèle COM distribué permet d’empaqueter des objets en tant qu’applications de service, en synchronisant COM avec les puissantes fonctionnalités d’intégration d’administration et de système de Windows.

> [!Note]  
> Dans cette documentation, l’acronyme COM est utilisé de préférence à DCOM. Cela est dû au fait que DCOM n’est pas séparé ; il s’agit simplement de COM avec un câble plus long. Dans les cas où la description est une opération à distance, le terme *com distribué* est utilisé.

 

COM est conçu pour permettre l’ajout de la prise en charge de la transparence d’emplacement qui s’étend sur un réseau. Il permet aux applications écrites pour des ordinateurs uniques de s’exécuter sur un réseau et fournit des fonctionnalités qui étendent ces fonctionnalités et ajoutent à la sécurité nécessaire dans un réseau. (Pour plus d’informations, consultez [sécurité dans com](security-in-com.md).)

COM spécifie un mécanisme par lequel le code de la classe peut être utilisé par de nombreuses applications différentes.

Pour plus d'informations, voir les rubriques suivantes :

-   [Obtention d’un pointeur vers un objet](getting-a-pointer-to-an-object.md)
-   [Création d’un objet à l’aide d’un objet de classe](creating-an-object-through-a-class-object.md)
-   [Responsabilités du serveur COM](com-server-responsibilities.md)
-   [État persistant de l’objet](persistent-object-state.md)
-   [Fournir des informations sur la classe](providing-class-information.md)
-   [Communication entre les objets](inter-object-communication.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Synchronisation des appels](call-synchronization.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




