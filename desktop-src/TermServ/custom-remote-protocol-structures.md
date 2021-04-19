---
title: Structures du fournisseur protocole RDP (Remote Desktop Protocol)
description: L’API de protocole distant personnalisé prend en charge les structures suivantes.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106541580"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Structures du fournisseur protocole RDP (Remote Desktop Protocol)

L’API de protocole distant personnalisé prend en charge les structures suivantes.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**\_ \_ données de support TSMF \_ dans**](tsmf-support-data-in.md)
</dt> <dd>

Contient des informations sur les formats multimédias.

</dd> <dt>

[**TSMF \_ prennent en charge \_ \_ les données sortantes**](tsmf-support-data-out.md)
</dt> <dd>

Contient des informations sur les formats multimédias.

</dd> <dt>

[**TSMF \_ prend en charge \_ NODEDATA \_ dans**](tsmf-support-nodedata-in.md)
</dt> <dd>

Utilisé à l’intérieur des [**\_ \_ données \_ de prise en charge TSMF dans**](tsmf-support-data-in.md) la structure pour contenir des informations sur les formats multimédias pris en charge.

</dd> <dt>

[**TSMF \_ support \_ NODEDATA \_ out**](tsmf-support-nodedata-out.md)
</dt> <dd>

Utilisé dans la structure de [**données de prise en charge de TSMF pour contenir des informations sur \_ \_ \_ les**](tsmf-support-data-out.md) formats multimédias pris en charge.

</dd> <dt>

[**\_paramètres de connexion Wrds \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Contient les informations de paramètres de connexion pour une session à distance.

</dd> <dt>

[**\_Paramètres de connexion Wrds \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Contient les informations de paramètres de connexion pour une session à distance.

</dd> <dt>

[**\_ \_ \_ informations sur les fuseaux horaires dynamiques Wrds \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Contient des informations sur les fuseaux horaires dynamiques.

</dd> <dt>

[**paramètres de l' \_ écouteur Wrds \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Contient les informations de paramètre de l’écouteur pour une session à distance.

</dd> <dt>

[**Paramètres de l' \_ écouteur Wrds \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Contient les paramètres d’écouteur pour une session à distance.

</dd> <dt>

[**\_paramètres Wrds**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Contient des informations de paramètre relatives à la stratégie pour une session à distance.

</dd> <dt>

[**\_Paramètres Wrds \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Contient les paramètres liés à la stratégie pour une session à distance.

</dd> <dt>

[**\_statistiques du cache WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Contient des statistiques de cache de protocole.

</dd> <dt>

[**WTS \_ afficher l' \_ IOCTL**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Contient des informations sur l’affichage du client.

</dd> <dt>

[**\_données du client WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Contient des informations sur la connexion cliente.

</dd> <dt>

[**\_fonctionnalités de licence WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Contient des informations sur les fonctionnalités de licence du client.

</dd> <dt>

[**\_données de stratégie WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Contient les informations de stratégie transmises par le service Services Bureau à distance au protocole.

</dd> <dt>

[**valeur de la \_ propriété WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Contient des informations sur une valeur de propriété à récupérer à partir du protocole.

</dd> <dt>

[**\_cache de protocole WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Contient le nombre de lectures du cache et de présences dans le cache.

</dd> <dt>

[**\_compteurs de protocole WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Contient des compteurs de performance de protocole.

</dd> <dt>

[**\_État du protocole WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Contient des informations sur l’état du protocole.

</dd> <dt>

[**\_État du service WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Contient des informations sur les modifications de l’état du service Services Bureau à distance.

</dd> <dt>

[**\_ID de session WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Contient un **GUID** qui identifie de façon unique une session.

</dd> <dt>

[**WTS \_ petit \_ Rect**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Contient les coordonnées de la fenêtre cliente.

</dd> <dt>

[**WTS \_ sockaddr**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Contient une adresse de Socket.

</dd> <dt>

[**WTS \_ SystemTime**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Spécifie les informations de date et d’heure pour les transitions entre l’heure d’hiver et l’heure d’été.

</dd> <dt>

[**WTS \_ les \_ informations de fuseau horaire \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Contient des informations sur les fuseaux horaires du client.

</dd> <dt>

[**\_ \_ informations d’identification de l’utilisateur WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Contient les informations d’identification d’un utilisateur.

</dd> <dt>

[**\_données utilisateur \_ WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Contient des valeurs de propriété de client sélectionnées.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-reference.md)
</dt> <dt>

[Énumérations du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Interfaces du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Unions de fournisseurs protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




