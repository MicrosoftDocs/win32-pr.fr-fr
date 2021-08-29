---
title: Système de nom de domaine
description: DNS (domain Name System), un service de localisation dans Microsoft Windows, est un protocole standard qui localise les ordinateurs sur un réseau basé sur IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS, (voir Domain Name System)
- Système de nom de domaine
- Domain Name System, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9762fd6a46b9fe0fd07b5b75a8e06c31819100b5548a51286ef753cf43447888
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825339"
---
# <a name="domain-name-system"></a>Système de nom de domaine

## <a name="purpose"></a>Objectif

DNS (domain Name System), un service de localisation dans Microsoft Windows, est un protocole standard qui localise les ordinateurs sur un réseau basé sur IP. les réseaux IP, tels que les réseaux Internet et Windows, s’appuient sur des adresses basées sur des nombres pour traiter les données. Toutefois, les utilisateurs peuvent plus facilement mémoriser les adresses de noms. il est donc nécessaire de traduire des noms conviviaux (tels que `www.microsoft.com` ) en adresses reconnues par le réseau (par exemple, composées).

## <a name="where-applicable"></a>Le cas échéant

Windows et Active Directory utilisent DNS. dns est le service de localisation principal pour Internet et Active Directory, et par conséquent, dns est considéré comme un service de base pour Windows et Active Directory.

## <a name="developer-audience"></a>Développeurs concernés

Windows fournit des fonctions qui permettent aux programmeurs d’applications d’utiliser dns, tels que la requête dns par programmation, la comparaison d’enregistrements et la recherche de nom.

Les composants DNS programmables sont conçus pour être utilisés par les programmeurs C/C++. Vous devez être familiarisé avec la mise en réseau et DNS. Les programmeurs doivent être familiarisés avec la suite de protocoles IP, ainsi que le protocole DNS et les opérations DNS.

## <a name="run-time-requirements"></a>Conditions d’exécution

DNS est utilisé sur tous les réseaux IP qui requièrent un service de localisation compatible avec Internet. toutefois, l’API DNS requiert Windows 2000 ou une version ultérieure.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                             | Description                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Documents de normes DNS](dns-standards-documents.md)<br/> | Liens vers les documents de normes DNS publics.<br/>                                  |
| [À propos de DNS](about-dns.md)<br/>                             | Informations générales sur DNS.<br/>                                            |
| [Référence DNS](dns-reference.md)<br/>                     | Documentation de référence pour DNS.<br/>                                          |
| [Fournisseur WMI DNS](dns-wmi-provider.md)<br/>               | Informations générales et documentation de référence pour le fournisseur WMI DNS.<br/> |
| [Glossaire](glossary-gly.md)<br/>                           | Glossaire des termes et définitions DNS.<br/>                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Assistance du protocole Internet](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

[Services d'annuaire](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)
</dt> </dl>

 

