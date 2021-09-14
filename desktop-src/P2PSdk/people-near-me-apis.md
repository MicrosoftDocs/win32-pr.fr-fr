---
description: API voisinage immédiat
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: API voisinage immédiat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194299"
---
# <a name="people-near-me-apis"></a>API voisinage immédiat

Toutes les applications capables de voisinage [immédiat](about-people-near-me.md) (PNM) peuvent utiliser les API Win32 suivantes :

### <a name="contacts-api"></a>API contacts

L’API contacts permet d’accéder aux informations de contact de l’utilisateur connecté, de récupérer des informations sur les contacts précédemment stockés ou de stocker les informations de contact et le certificat numérique d’un nouveau contact.

### <a name="people-near-me-api"></a>API voisinage immédiat

L’API PNM est utilisée pour rechercher les utilisateurs à proximité, leurs centres d’intérêt publiés, les objets arbitraires qu’ils choisissent de publier et les applications publiées.

### <a name="publication-api"></a>API de publication

L’API de publication est utilisée pour interagir avec les contacts distants. La couche de [signalisation d’homologue](windows-peer-components-for-people-near-me.md) utilisée par le gestionnaire de publication est également utilisée par le module PNM pour établir des connexions.

### <a name="invitation-api"></a>API d’invitation

L’API d’invitation est utilisée par une application de collaboration pour inviter un ou plusieurs homologues spécifiques dans une activité de collaboration.

### <a name="application-registration-api"></a>API d’inscription des applications

L’API d’inscription d’application est utilisée par le programme d’installation d’une application de collaboration pour inscrire l’application. Une application qui prend en charge PNM demandera à l’utilisateur pendant le processus d’installation de déterminer si l’application doit être mise à la disposition des utilisateurs sur le sous-réseau.

 

 



