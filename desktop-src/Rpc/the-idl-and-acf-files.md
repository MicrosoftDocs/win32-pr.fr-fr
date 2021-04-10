---
title: Fichiers IDL et ACF
description: La syntaxe du Microsoft Interface Definition Language (MIDL) est basée sur la syntaxe du langage de programmation C. Quand un concept de langage dans cette description de MIDL n’est pas entièrement défini, la définition de langage C de ce terme est implicite.
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- Appel de procédure distante RPC, description, fichiers IDL et ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7f739e50fd4e04ae35a11adcbbc936cd3cb36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941190"
---
# <a name="the-idl-and-acf-files"></a>Fichiers IDL et ACF

La syntaxe du Microsoft Interface Definition Language (MIDL) est basée sur la syntaxe du langage de programmation C. Quand un concept de langage dans cette description de MIDL n’est pas entièrement défini, la définition de langage C de ce terme est implicite.

La conception MIDL spécifie deux fichiers distincts : le fichier IDL (Interface Definition Language) et le fichier de configuration de l’application (ACF). Ces fichiers contiennent des attributs qui dirigent la génération des fichiers stub du langage C qui gèrent l’appel de procédure distante (RPC). Le fichier IDL contient une description de l’interface entre le client et les programmes serveur. Les applications RPC utilisent le fichier ACF pour décrire les caractéristiques de l’interface qui sont spécifiques au matériel et au système d’exploitation qui composent un environnement d’exploitation particulier. La Division de ces informations en deux fichiers permet de séparer l’interface logicielle des caractéristiques qui affectent uniquement l’environnement d’exploitation.

Le fichier IDL spécifie un contrat réseau entre le client et le serveur, c’est-à-dire que le fichier IDL spécifie ce qui est transmis entre le client et le serveur. La conservation de ces informations à partir des informations relatives à l’environnement d’exploitation rend le fichier IDL portable dans d’autres environnements. Le fichier IDL se compose de deux parties : un [en-tête d’interface](the-idl-interface-header.md) et un [corps d’interface](the-idl-interface-body.md).

Le ACF spécifie des attributs qui affectent uniquement les performances locales plutôt que le contrat réseau. Microsoft RPC vous permet de combiner les attributs ACF et IDL dans un seul fichier IDL. Vous pouvez également combiner plusieurs interfaces dans un seul fichier IDL (et son ACF).

Cette section résume les attributs qui sont spécifiés dans les fichiers IDL et ACF. Elle est destinée à fournir uniquement une vue d’ensemble. Pour plus d’informations, consultez les informations de référence sur le [langage MIDL](/windows/desktop/Midl/midl-language-reference)et la [référence de Command-Line MIDL](/windows/desktop/Midl/midl-command-line-reference). La description de cette section est présentée dans les rubriques suivantes :

-   [Fichier IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
-   [Fichier de configuration de l’application (ACF)](the-application-configuration-file-acf-.md)
-   [Sortie du compilateur MIDL](midl-compiler-output.md)

 

 