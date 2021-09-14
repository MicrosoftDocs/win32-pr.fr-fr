---
title: Espaces de noms
description: Les objets qui résident dans un espace de noms donné sont identifiés par un nom unique.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- espaces de noms ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854025"
---
# <a name="namespaces"></a>Espaces de noms

Les objets qui résident dans un espace de noms donné sont identifiés par un nom unique. Par exemple, les fichiers stockés sur un lecteur de disque PC résident dans l’espace de noms du système de fichiers. Le nom unique d’un fichier est basé sur l’emplacement où il est stocké dans l’espace de noms du système de fichiers. Par exemple :


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Les espaces de noms de service d’annuaire identifient également les objets qu’ils contiennent par des noms uniques qui sont généralement basés sur l’emplacement dans le répertoire où se trouve l’objet. Par exemple, dans un répertoire X. 500, un objet donné peut avoir un nom semblable à ce qui suit :


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Différents services d’annuaire utilisent des formes différentes pour nommer les objets qu’ils contiennent. Cela complique le traitement de différents espaces de noms, en particulier pour les développeurs, en tenant compte de tous les environnements sur lesquels le code est en cours d’exécution.

L’un des objectifs de l’interface ADSI (Active Directory Service Interfaces) est de fournir une infrastructure d’attribution de noms qui permet d’accéder aux espaces de noms de différents fournisseurs de services d’annuaire.

ADSI définit une convention d’affectation de noms qui permet d’identifier de manière unique un objet dans un environnement hétérogène. Ces noms sont appelés chaînes ADsPath. Les chaînes ADsPath prennent plusieurs formes :


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



des formats ADsPath supplémentaires peuvent être introduits par différents fournisseurs adsi (tels que le fournisseur adsi pour le serveur Internet Information Services, qui prend en charge le ADsPaths « IIS:// »).

 

 




