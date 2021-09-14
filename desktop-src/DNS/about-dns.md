---
title: À propos de DNS
description: Le système DNS (Domain Name System) est un protocole standard utilisé pour localiser des ordinateurs sur un réseau basé sur IP. Les utilisateurs peuvent mémoriser les noms complets, tels que www.microsoft.com, comme les adresses basées sur les nombres, telles que composées.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- À propos du système DNS (Domain Name System)
- DNS (Domain Name System), à propos de
- DNS (Domain Name System), Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114705"
---
# <a name="about-dns"></a>À propos de DNS

Le système DNS (Domain Name System) est un protocole standard utilisé pour localiser des ordinateurs sur un réseau basé sur IP. Les utilisateurs peuvent se souvenir de noms complets, par exemple `www.microsoft.com` plus faciles que les adresses basées sur les nombres, tels que composées.

les réseaux IP, tels que les réseaux Internet et Windows, s’appuient sur des adresses basées sur des nombres pour transmettre des données à travers le réseau. par conséquent, il est nécessaire de traduire les noms d’affichage (tels que `www.microsoft.com` ) en adresses numériques que le réseau peut reconnaître (par exemple, composées). DNS est le service de choix dans Windows pour localiser ces ressources et les traduire en adresses IP.

dns est le service de localisation principal pour Active Directory. par conséquent, dns peut être considéré comme un service de base pour les Windows et les Active Directory. Windows fournit des fonctions qui permettent aux programmeurs d’applications d’utiliser des fonctions dns telles que la création de requêtes dns par programmation, la comparaison d’enregistrements et la recherche de noms.

De nombreuses fonctions DNS sont en fait des types de fonction, car il existe un nom de base pour la fonction, mais son utilisation dépend de l’encodage des caractères. Par exemple, la fonction [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) est indiquée dans la référence de fonction de l’interface de programmation d’applications (API) DNS en tant que **DNSQuery**, toutefois, son utilisation dans les applications varie selon que l’encodage de caractères est ANSI (désigné par l’ajout \_ d’un au nom du type de fonction), Unicode (désigné par l’ajout de \_ W au nom du type de fonction) ou UTF-8 (désigné par \_ l’ajout de UTF au nom du type de fonction). Par conséquent, l’appel de fonction pour la fonction **DNSQuery** serait en fait l’un des suivants :

DnsQuery \_ a ( \_ codage ANSI)

DnsQuery \_ w ( \_ w pour l’encodage Unicode)

DnsQuery \_ UTF8 ( \_ UTF8 pour l’encodage UTF-8)

Toutes les fonctions qui requièrent cette Convention indiquent clairement cette exigence dans les premières phrases de leur définition de fonction. Utilisez le nom de fonction approprié ; par exemple, vous ne pouvez pas simplement appeler [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) au lieu de DNSQuery \_ A.

 

 




