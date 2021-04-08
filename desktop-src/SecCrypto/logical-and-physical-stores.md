---
description: Les magasins système par défaut, y compris MY, CA et ROOT, sont implémentés en tant que magasins de collection logique avec un certain nombre de magasins physiques prédéfinis en tant que membres stockés.
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: Magasins logiques et physiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752140"
---
# <a name="logical-and-physical-stores"></a>Magasins logiques et physiques

Les magasins système par défaut, y compris MY, CA et ROOT, sont implémentés en tant que magasins de collection logique avec un certain nombre de magasins physiques prédéfinis en tant que membres stockés. Les magasins physiques de membres d’un magasin système s’ouvrent automatiquement lorsque le magasin système est ouvert. Un utilisateur peut ajouter des magasins physiques supplémentaires à n’importe quel regroupement du magasin système. La fonction CryptoAPI [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) ajoute un nouveau magasin physique à une collection du magasin système. [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) dissocie un magasin physique d’un magasin de système logique. [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) crée un nouveau magasin système sous un HKEY de Registre, tandis que [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) supprime un magasin système du Registre.

Dans CryptoAPI, les magasins système sont des magasins logiques avec des magasins physiques associés. Tous les certificats dans un magasin système existant restent disponibles et l’ajout physique de nouveaux certificats est effectué dans les magasins physiques qui composent le magasin de système logique.

Les utilisateurs qui préfèrent continuer à utiliser des magasins système physiques et ne pas effectuer de conversion en magasins logiques peuvent ouvrir des magasins système avec le \_ \_ fournisseur de Registre système Proven Store \_ \_ . Ce fournisseur continuera à utiliser chaque magasin système comme un magasin physique unique.

Les fonctions [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation), [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)et [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) répertorient les emplacements des magasins système, les magasins système disponibles et tous les magasins physiques qui sont membres d’un magasin système.

Les magasins système peuvent également être déplacés. Par défaut, un magasin système est ouvert par rapport à une sous-clé de Registre selon un modèle prédéfini. Pour plus d’informations, consultez [emplacements du magasin système](system-store-locations.md). La définition de l' \_ \_ \_ indicateur de relocalisation du magasin système du certificat \_ dans le paramètre *dwFlags* passé à [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) place un magasin système dans le Registre sous une sous-clé de Registre spécifiée par l’utilisateur au lieu de celle prédéfinie.

 

 



