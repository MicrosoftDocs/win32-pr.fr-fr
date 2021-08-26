---
title: Fichiers composés asynchrones
description: Les fichiers composés asynchrones, l’implémentation fournie par le système du stockage asynchrone, permettent le téléchargement efficace des fichiers composés à partir d’Internet en général et du Web en particulier.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15404f33041fb52f5baa5230f69434ce390b985c41374235c1f3979ef6c2f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034983"
---
# <a name="asynchronous-compound-files"></a>Fichiers composés asynchrones

Les fichiers composés asynchrones, l’implémentation fournie par le système du stockage asynchrone, permettent le téléchargement efficace des fichiers composés à partir d’Internet en général et du Web en particulier. L’architecture de base des fichiers composés asynchrones est présentée dans le diagramme suivant.

![architecture de base des fichiers composés asynchrones](images/asy-stor.png)

L’implémentation de fichiers composés asynchrones peut fonctionner avec de nouveaux types de moniker asynchrones qui comprennent les protocoles Internet et peuvent établir une liaison à un objet identifié par une URL. Un tel moniker retourne un pointeur [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ou [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) asynchrone à partir de l’appel du client à [**IMoniker :: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage).

En général, les fichiers composés sont implémentés en plus d’un objet de tableau d’octets, une abstraction d’un fichier qui représente les données d’un objet sous la forme d’un tableau d’octets plat. L’objet tableau d’octets expose ses fonctionnalités via l’interface [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) . Si un tableau d’octets prend en charge le stockage asynchrone non bloquant, il retourne E \_ en attente à l’implémentation du fichier composé, qui à son tour propage l’erreur à l’appelant.

Pour assurer le suivi des données disponibles pendant un téléchargement, un tableau d’octets qui prend en charge le stockage asynchrone expose l’interface [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) sur un objet wrapper fourni par le système spécifiquement à cet effet. Le code de téléchargement fourni par un moniker asynchrone appelle cette interface pour remplir le tableau d’octets de manière asynchrone, à mesure que les données sont disponibles. L’objet wrapper expose également une interface **ILockBytes** , que l’implémentation de fichiers composés asynchrone utilise pour lire et écrire des données depuis et vers le tableau.

Les objets de flux et de stockage asynchrones fournissent un point de connexion pour l’interface [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) , qui est implémentée par le code de téléchargement du moniker asynchrone. L’implémentation de fichiers composés asynchrones appelle **IProgressNotify** pour fournir au téléchargeur des informations sur l’état de l’opération de téléchargement.

 

 