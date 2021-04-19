---
title: Utilisation de StoServe
description: StoServe est une DLL destinée principalement à un serveur COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513540"
---
# <a name="using-stoserve"></a>Utilisation de StoServe

**StoServe** est une dll destinée principalement à un serveur com. Bien qu’il puisse être chargé implicitement par liaison à son associé. Fichier LIB, il est normalement utilisé après un appel de LoadLibrary explicite, généralement à partir de la fonction COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **StoServe** est un serveur in-process à inscription automatique.

Pour utiliser **StoServe**, un programme client n’a pas besoin d’inclure StoServe. H ou lien vers STOSERVE. LIB. Un client COM de **StoServe** obtient l’accès uniquement via le CLSID de son objet et les services com. Pour **StoServe**, le CLSID est CLSID \_ DllPaper (défini dans le fichier PAPGUIDS. H dans le \\ répertoire frère Inc). L’exemple de code [StoClien](structured-storage-client-sample--stoclien-.md) montre comment le client obtient cet accès.

Le Makefile qui génère cet exemple inscrit automatiquement le serveur dans le registre. Vous pouvez lancer manuellement son inscription automatique en émettant la commande suivante à l’invite de commandes dans le répertoire **StoServe** :

 **registre** NMAKE

Cela suppose que vous disposez d’un environnement de compilation configuré. Si ce n’est pas le cas, vous pouvez également appeler directement la commande REGISTER.EXE à l’invite de commandes dans le répertoire **StoServe** .

**..\\ inscrire \\register.exe** **stoserve.dll**

Ces commandes d’inscription requièrent une version antérieure de l’exemple REGISTER de cette série, ainsi qu’une version antérieure de STOSERVE.DLL.

Dans cette série, les Makefiles utilisent l’utilitaire REGISTER.EXE à partir de l’exemple REGISTER. Les versions récentes du kit de développement logiciel (SDK) de la plateforme et de Visual C++ incluent un utilitaire, REGSVR32.EXE, qui peut être utilisé de la même manière pour inscrire des serveurs in-process et marshaler des dll.

**StoServe** utilise de nombreux services et classes utilitaires fournis par apputil. Pour plus d’informations sur APPUTIL, examinez le code source de la bibliothèque APPUTIL dans le répertoire APPUTIL frère et APPUTIL.HTM dans le répertoire principal du didacticiel.

 

 