---
title: COM, DCOM et les bibliothèques de types
description: Le modèle COM (Component Object Model) et le modèle DCOM (Distributed Component Object Model) utilisent des appels de procédure distante (RPC) pour permettre aux objets de composants distribués de communiquer entre eux.
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- interfaces MIDL, COM
- interfaces MIDL, DCOM
- interfaces MIDL, bibliothèques de types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f0b21aad9f88f02d8029d478eead50f5501ecc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842221"
---
# <a name="com-dcom-and-type-libraries"></a>COM, DCOM et les bibliothèques de types

Le modèle COM (Component Object Model) et le modèle DCOM (Distributed Component Object Model) utilisent des appels de procédure distante (RPC) pour permettre aux objets de composants distribués de communiquer entre eux. Par conséquent, une interface COM ou DCOM définit l’identité et les caractéristiques externes d’un objet COM. Il forme les moyens par lesquels les clients peuvent accéder aux méthodes et aux données d’un objet. Avec DCOM, cet accès est possible, que les objets existent dans le même processus, que des processus différents sur le même ordinateur ou sur des ordinateurs différents. Comme avec les interfaces client/serveur RPC, un objet COM ou DCOM peut exposer ses fonctionnalités de différentes façons et via plusieurs interfaces.

## <a name="type-library"></a>Bibliothèque de types

Une bibliothèque de types (. tlb) est un fichier binaire qui stocke des informations sur les propriétés et méthodes d’un objet COM ou DCOM dans un formulaire accessible à d’autres applications au moment de l’exécution. À l’aide d’une bibliothèque de types, une application ou un navigateur peut déterminer les interfaces prises en charge par un objet et appeler les méthodes d’interface d’un objet. Cela peut se produire même si l’objet et les applications clientes ont été écrits dans des langages de programmation différents. L’environnement d’exécution COM/DCOM peut également utiliser une bibliothèque de types pour fournir un marshaling automatique inter-cloisonnement, inter-processus et inter-ordinateurs pour les interfaces décrites dans les bibliothèques de types.

## <a name="characteristics-of-an-interface"></a>Caractéristiques d’une interface

Vous définissez les caractéristiques d’une interface dans un fichier de définition d’interface (IDL) et un fichier de configuration d’application facultatif (ACF) :

-   Le fichier IDL spécifie les caractéristiques des interfaces de l’application sur le câble, c’est-à-dire la façon dont les données doivent être transmises entre le client et le serveur, ou entre les objets COM.
-   Le fichier ACF spécifie les caractéristiques de l’interface, telles que les handles de liaison, qui se rapportent uniquement à l’environnement d’exploitation local. Le fichier ACF peut également spécifier comment marshaler et transmettre une structure de données complexe dans un format indépendant de l’ordinateur.

Pour plus d’informations sur les fichiers IDL et ACF, consultez [les fichiers IDL et ACF](/windows/desktop/Rpc/the-idl-and-acf-files).

Les fichiers IDL et ACF sont des scripts écrits en Microsoft Interface Definition Language (MIDL), qui est l’implémentation Microsoft et l’extension du langage IDL (Interface Definition Language) OSF-DCE. Les extensions Microsoft du langage IDL vous permettent de créer des interfaces COM et des bibliothèques de types. Le compilateur, Midl.exe, utilise ces scripts pour générer des stubs et des fichiers d’en-tête de langage C, ainsi que des fichiers de bibliothèque de types.

## <a name="the-midl-compiler"></a>Compilateur MIDL

En fonction du contenu de votre fichier IDL, le compilateur MIDL génère l’un des fichiers suivants.

Un fichier proxy/stub en langage C, un fichier d’identificateur d’interface, un fichier de données DLL et un fichier d’en-tête associé pour une interface COM personnalisée. Le compilateur MIDL génère ces fichiers lorsqu’il rencontre l’attribut d’objet dans une liste d’attributs d’interface. Pour plus d’informations sur ces fichiers, consultez [fichiers générés pour une interface com](files-generated-for-a-com-interface.md).

Fichier de bibliothèque de types compilé (. tlb) et fichier d’en-tête associé. MIDL génère ces fichiers lorsqu’il rencontre une instruction [**Library**](library.md) dans le fichier IDL. Pour obtenir des informations générales sur les bibliothèques de types, consultez le [contenu d’une bibliothèque de types](/previous-versions/windows/desktop/automat/contents-of-a-type-library)dans le Guide de référence du programmeur Automation.

C/C++-fichiers du client et du serveur stub du langage et fichier d’en-tête associé pour une interface RPC. Ces fichiers sont générés lorsque des interfaces dans le fichier IDL n’ont pas l’attribut d' [**objet**](object.md) . Pour obtenir une vue d’ensemble des fichiers stub et d’en-tête, consultez [procédure de génération générale](/windows/desktop/Rpc/general-build-procedure). Pour plus d’informations, consultez [fichiers générés pour une interface RPC](files-generated-for-an-rpc-interface.md).

 

 