---
description: Les fournisseurs WMI de sécurité peuvent être utilisés pour les scripts WMI et pour créer un fournisseur de sécurité managé.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Fournisseurs WMI de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517249"
---
# <a name="security-wmi-providers"></a>Fournisseurs WMI de sécurité

## <a name="purpose"></a>Objectif

Les fournisseurs WMI de sécurité permettent aux administrateurs et aux programmeurs de configurer Chiffrement de lecteur BitLocker (BDE) et le Module de plateforme sécurisée (TPM) (TPM) à l’aide d’Windows Management Instrumentation (WMI).

## <a name="developer-audience"></a>Développeurs concernés

Ce document spécifie l’interface du fournisseur WMI pour la gestion et la configuration de Chiffrement de lecteur BitLocker (BDE) et Module de plateforme sécurisée (TPM) (TPM) sur Windows Server 2008 R2 et Windows Server 2008 pour les serveurs, et Windows 7 et Windows Vista pour les ordinateurs clients. Elle est destinée à être lue par les scripts d’écriture, les éléments de l’interface utilisateur ou d’autres outils d’administration pour BDE ou le TPM.

## <a name="run-time-requirements"></a>Conditions d’exécution

Les fournisseurs WMI de sécurité requièrent le fichier. mof spécifié avec chaque fournisseur et un système d’exploitation pris en charge. Le système d’exploitation minimal est Windows Server 2008 ou Windows Vista. Chiffrement de lecteur BitLocker est disponible uniquement pour les versions Windows Vista entreprise et Windows Vista Édition intégrale de Windows Vista. Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                               | Description                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [À propos des fournisseurs WMI de sécurité](about-security-wmi-providers.md)<br/>         | Bref aperçu des fournisseurs WMI de sécurité.<br/>           |
| [Informations de référence sur les fournisseurs WMI de sécurité](security-wmi-providers-reference.md)<br/> | Documentation de référence pour les fournisseurs WMI de sécurité.<br/> |



 

## <a name="additional-resources"></a>Ressources supplémentaires

Vous trouverez ci-dessous des ressources supplémentaires.



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classes<br/> | Pour plus d’informations sur les fournisseurs WMI de sécurité, consultez [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) et [**Win32 \_ TPM**](win32-tpm.md).<br/> |



 

 

 




