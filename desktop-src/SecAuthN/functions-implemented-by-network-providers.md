---
description: Les fonctions suivantes sont implémentées par une DLL de fournisseur réseau pour communiquer avec le routeur de fournisseur multiple (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Fonctions implémentées par les fournisseurs de réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892bcb5c19f54e5de667eb72119f6b9e5fc9b183b8d5038ce37b7e556ae5d3a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016319"
---
# <a name="functions-implemented-by-network-providers"></a>Fonctions implémentées par les fournisseurs de réseau

Les fonctions suivantes sont implémentées par une DLL de fournisseur réseau pour communiquer avec le [*routeur de fournisseur multiple*](/windows/desktop/SecGloss/m-gly) (MPR). Notez que seules les [fonctions de fonctionnalités](capabilities-functions.md) doivent être implémentées par un fournisseur réseau. L’implémentation des autres types de fonctions est facultative et dépend des exigences du fournisseur réseau.



| Ensemble de fonctions                                                                                    | Description                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fonctions fonctions](capabilities-functions.md)<br/>                                 | Permet à l’appelant de déterminer les fonctionnalités du fournisseur réseau.<br/>                                                                |
| [Fonctions de nom d’utilisateur](user-name-functions.md)<br/>                                       | Demande au fournisseur réseau le nom d’utilisateur associé à une connexion.<br/>                                                            |
| [Fonctions de redirection de l’appareil](device-redirecting-functions.md)<br/>                     | Permet à un fournisseur réseau de rediriger des appareils, des lettres de lecteur et des ports LPT standard sur le système d’exploitation Microsoft MS-DOS.<br/> |
| [Fonctions de boîte de dialogue spécifiques au fournisseur](provider-specific-dialog-box-functions.md)<br/> | Permet à un fournisseur de réseau d’afficher ou d’agir sur des informations spécifiques au réseau.<br/>                                                            |
| [Fonctions d’administration](administrative-functions.md)<br/>                             | Permet à un fournisseur de réseau d’afficher ou d’agir sur des répertoires réseau spéciaux.<br/>                                                             |
| [Fonctions d’énumération](enumeration-functions.md)<br/>                                   | Permet à l’utilisateur de parcourir les ressources réseau.<br/>                                                                                            |



 

Pour plus d’informations sur la création et l’inscription d’un fournisseur de réseau, consultez [implémentation d’un fournisseur de réseau](implementing-a-network-provider.md) et [inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification](registering-network-providers-and-credential-managers.md).

 

