---
title: Fonctions TBS
description: TBS fournit les fonctions suivantes.
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- Services de base TPM (TBS), fonctions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193615"
---
# <a name="tbs-functions"></a>Fonctions TBS

TBS fournit les fonctions suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Création de contexte Tbsi \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | Crée un handle de contexte qui peut être utilisé pour passer des commandes à TBS.<br/>                                                                               |
| [**Tbsi \_ créer \_ une attestation \_ à partir du \_ Journal**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))<br/> | Crée une attestation en extrayant un TrustPoint à partir d’un journal TCG.<br/>                                                                                |
| [**Tbsi \_ GetDeviceInfo**](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | Obtient la version du module de plateforme sécurisée sur l’ordinateur.<br/>                                                                                                  |
| [**Tbsi \_ Obtient \_ origine**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | Récupère l’autorisation du propriétaire du module de plateforme sécurisée si les informations sont disponibles dans le registre local. <br/>                                             |
| [**Tbsi \_ récupérer \_ le \_ Journal TCG**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | récupère le dernier journal de Configuration de démarrage Windows (WBCL), également appelé journal TCG.<br/>                                                  |
| [**Tbsi \_ récupérer \_ le \_ Journal TCG \_ ex**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | obtient le Windows journal de Configuration de démarrage (WBCL), également appelé « journal TCG », du type spécifié.<br/>                                          |
| [**Tbsi \_ récupérer \_ les \_ journaux TCG**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))<br/>                                | obtenir un ou plusieurs Windows journaux de Configuration de démarrage (WBCL), également appelés journaux TCG.<br/>                                                        |
| [**\_Commande de \_ présence \_ physique Tbsi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | Passe une commande ACPI de présence physique via TBS au pilote.<br/>                                                                               |
| [**\_Attestation Tbsi Revoke \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | Invalide le PCR si le pilote ELAM détecte une violation de stratégie (un rootkit, par exemple).<br/>                                                     |
| [**Tbsip \_ annuler les \_ commandes**](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | Annule toutes les commandes en attente pour le contexte spécifié.<br/>                                                                                      |
| [**\_ \_ Fermer le contexte Tbsip**](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | Ferme un handle de contexte, qui libère les ressources associées au contexte dans TBS et ferme le handle de liaison utilisé pour communiquer avec TBS.<br/> |
| [**Tbsip \_ \_ commande Envoyer**](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | Envoie une commande de Module de plateforme sécurisée (TPM) (TPM) aux services de base du module de plateforme sécurisée (TBS) pour le traitement.<br/>                                                       |



 

 

