---
description: Actions par des packages de sécurité qui ne sont pas pris en charge dans Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Restrictions concernant l’inscription et l’installation d’un package de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd10cd8e2e98d4dccfc3a6230c3daecaeb8fec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749612"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Restrictions concernant l’inscription et l’installation d’un package de sécurité

La suppression, le remplacement ou le renvoi de packages de sécurité de boîte de réception (par exemple, Kerberos ou NTLM) ne sont pas une action prise en charge dans Windows et, à compter du 10 janvier 2017, cela est évité. Des packages de sécurité tiers (SSP/APs) peuvent être ajoutés. Toutefois, Windows ne prend pas en charge la suppression des SSP/APs préconfigurés. Plus précisément, la modification du paramètre de Registre **HKLM \\ System \\ CurrentControlSet \\ Control \\ LSA \\ OSConfig \\ Security packages** n’a jamais été prise en charge.

À partir de Windows 8.1, les clients qui souhaitent fournir des fonctionnalités supplémentaires peuvent ajouter leurs packages de sécurité à l’aide du paramètre de Registre **HKLM \\ System \\ CurrentControlSet \\ Control \\ LSA \\ Security packages** ([Registering SSP/AP dll](registering-ssp-ap-dlls.md)) et le paramètre de Registre associé **SecurityProviders** ([Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md)), le cas échéant. En outre, l’objectif des [packages de sécurité](../secgloss/s-gly.md#_security_security_package_gly) est d’implémenter de nouveaux protocoles de *sécurité* qui peuvent se présenter sous la forme d’un fournisseur SSP (Security Support Provider) ou d’un [package d’authentification](../secgloss/a-gly.md#_security_authentication_package_gly) (AP). L’objectif d’un SSP est de fournir une *connexion authentifiée*, une *intégrité de message* et des services de *chiffrement de message* qui ne sont pas encore pris en charge dans le système, tandis qu’un point d’accès est utilisé pour ajouter une nouvelle *logique d’authentification* utilisée pour déterminer s’il faut autoriser un utilisateur à se connecter.

Microsoft est investi dans la sécurité des clients et tente de s’assurer que les processus critiques tels que les SSP et les APs ne sont pas facilement amovibles du système. Par conséquent, le paramètre de Registre **HKLM \\ System \\ CurrentControlSet \\ Control \\ LSA \\ OSConfig \\ Security Packages** a été restreint à partir de Windows 8.1 afin d’empêcher toute modification. Pour faciliter la gestion des packages de sécurité tiers, les packages de sécurité de l' **\\ autorité de \\ \\ \\ certification locale \\ du contrôle LSA du système HKLM** ont été définis comme paramètres désignés pour les fournisseurs de sécurité/APS personnalisés. Il est également recommandé que toutes les fonctionnalités des SSP/points d’accès personnalisés qui se trouvent en dehors de l’étendue des packages de sécurité définis par Microsoft soient supprimées de ces fournisseurs/APs personnalisés et que les packages de sécurité de la boîte de réception ne sont pas supprimés par un produit.

 

 
