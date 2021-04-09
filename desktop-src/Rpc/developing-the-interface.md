---
title: Développement de l’interface
description: Une interface RPC décrit les fonctions distantes implémentées par le programme serveur.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- Appel de procédure distante RPC, tâches, développement de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b6f720bcd492e784ad07fe20e221ac54951680
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102100"
---
# <a name="developing-the-interface"></a>Développement de l’interface

Une interface RPC décrit les fonctions distantes implémentées par le programme serveur. L’interface garantit que le client et le serveur communiquent à l’aide des mêmes règles lorsque le client appelle une procédure distante offerte par le serveur. Une interface se compose d’un nom d’interface, de certains attributs, de définitions de type ou de constante facultatives et d’un ensemble de déclarations de procédure. Chaque déclaration de procédure doit contenir un nom de procédure, un type de retour et une liste de paramètres.

Les interfaces sont définies dans le Microsoft Interface Definition Language (MIDL). Si vous êtes familiarisé avec C ou C++, les définitions d’interface MIDL vont paraître relativement simples. MIDL ressemble à C et C++ de nombreuses façons.

Lors du développement d’une application RPC, un éditeur de texte est utilisé pour définir l’interface et la stocker dans un fichier texte avec une extension. idl. Pour plus d’informations, consultez [les fichiers IDL et ACF](the-idl-and-acf-files.md). Le compilateur MIDL génère un fichier d’en-tête que votre programme inclue dans les fichiers sources du client et du serveur. Le compilateur MIDL génère également deux fichiers sources C. Vous compilez et liez l’une d’entre elles à votre programme client et l’autre à votre programme serveur. Ces deux fichiers sources C sont les stubs du client et du serveur. Pour obtenir une vue d’ensemble des stubs client et serveur, consultez fonctionnement de [RPC](how-rpc-works.md). Pour obtenir une vue d’ensemble du compilateur MIDL, consultez [compilation d’un fichier MIDL](using-midl.md).

Par défaut, le stub client et serveur portent le même nom, ce qui peut poser des problèmes si le client est lié au stub serveur, ou vice versa. L’utilisation de l’option [**/prefix**](/windows/desktop/Midl/-prefix) MIDL empêche l’apparition de cette erreur courante.

L’illustration suivante montre le processus de création d’une interface.

![la création de stubs client et serveur avec l’option/prefix empêche les problèmes de compilation accidentels](images/idldev.png)

Il est possible que vous deviez également spécifier un fichier de configuration d’application (ACF) pour l’entrée dans le compilateur MIDL. Pour plus d’informations sur les fichiers de configuration de l’application, consultez [les fichiers IDL et ACF](the-idl-and-acf-files.md).

En plus du compilateur MIDL, vous devez généralement utiliser l’utilitaire uuidgen pour générer un identificateur unique universel (UUID, interchangeable avec le terme GUID). Cette section contient des informations sur ces deux outils, répartis dans les rubriques suivantes :

-   [Génération d’UUID d’interface](generating-interface-uuids.md)
-   [Utilisation de MIDL](using-midl.md)

 

 