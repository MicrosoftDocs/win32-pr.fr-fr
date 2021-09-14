---
description: Lorsque le système informatique est démarré, l’autorité de sécurité locale (LSA) charge automatiquement toutes les dll du package d’authentification/fournisseur de services de sécurité (SSP/AP) inscrit dans son espace de processus. Les illustrations suivantes illustrent le processus d’initialisation.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Initialisation du mode LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123454"
---
# <a name="lsa-mode-initialization"></a>Initialisation du mode LSA

Lorsque le système informatique est démarré, l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) charge automatiquement toutes les dll du [](../secgloss/s-gly.md) / [*package d’authentification*](../secgloss/a-gly.md) du fournisseur de support de sécurité (SSP/AP) inscrit dans son espace de processus. Les illustrations suivantes illustrent le processus d’initialisation.

> [!Note]  
> « Kerberos » représente le SSP/AP Microsoft [*Kerberos*](../secgloss/k-gly.md) , et « mon SSP/AP » représente un SSP/AP personnalisé qui contient deux packages de sécurité personnalisés.

 

![initialisation du mode LSA](images/lsamode1.png)

Au démarrage, l’autorité LSA appelle la fonction [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) dans chaque fournisseur de services partagés/AP pour obtenir des pointeurs vers les fonctions implémentées par chaque [*package de sécurité*](../secgloss/s-gly.md) dans la dll. Les pointeurs de fonction sont passés à l’autorité LSA dans un tableau de structures de [**\_ \_ table de fonctions SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .

![l’autorité LSA appelle splsamodeinitialize pour recevoir des pointeurs de fonction](images/lsamode2.png)

Après avoir reçu l’ensemble de structures de [**\_ \_ table de fonctions SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , l’autorité LSA appelle la fonction de [**réinitialisation**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de chaque package de sécurité. Le LSA utilise cet appel de fonction pour passer chaque package de sécurité à une structure de [**\_ table de \_ fonctions \_ LSA SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , qui contient des pointeurs vers les fonctions de prise en charge LSA disponibles pour les packages de sécurité. En plus de stocker les pointeurs dans les fonctions de prise en charge LSA, les packages de sécurité personnalisés doivent utiliser leur implémentation de la fonction de **réinitialisation** pour effectuer tout traitement relatif à l’initialisation.

Pour obtenir la liste des fonctions de prise en charge LSA disponibles pour les packages de sécurité en mode LSA, voir [LSA Functions called by SSP/APS](authentication-functions.md).

Pour plus d’informations sur l’inscription d’une DLL SSP/AP, consultez [inscription de dll SSP/AP](registering-ssp-ap-dlls.md).

 

 
