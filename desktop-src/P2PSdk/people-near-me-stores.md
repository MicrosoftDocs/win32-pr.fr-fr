---
description: Personnes proches des boutiques
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Personnes proches des boutiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866694"
---
# <a name="people-near-me-stores"></a>Personnes proches des boutiques

Les applications capables de voisinage [immédiat](about-people-near-me.md) (PNM) peuvent utiliser les banques de données suivantes :

### <a name="windows-address-book"></a>Carnet d’adresses Windows

Le carnet d’adresses Windows stocke les informations sur les contacts et leurs certificats numériques. Le contact «**me**», représentant l’utilisateur actuellement connecté, est également stocké dans le carnet d’adresses Windows.

### <a name="certificate-store"></a>Magasin de certificats

Le magasin de certificats contient le certificat auto-signé pour le contact «**me**».

### <a name="application-store"></a>Boutique d'applications

Un programme d’installation d’application inscrit une application avec PNM pendant le processus d’installation. Il s’agit des objets qui peuvent être recherchés par d’autres utilisateurs lorsqu’ils tentent de se connecter à un utilisateur avec une application courante, par exemple un jeu d’ordinateurs. Pour chaque application, le magasin d’applications contient le nom de l’application, un identificateur global unique (GUID), une étendue de l’application, une description et un chemin d’accès au fichier exécutable du programme. L’étendue d’une application peut être définie sur aucun (non publié), voisinage immédiat (publié sur le sous-réseau local), contacts (publiés uniquement pour les contacts) ou tous (publié sur le sous-réseau local et pour les contacts). Le magasin d’applications se trouve dans le Registre Windows Vista.

 

 



