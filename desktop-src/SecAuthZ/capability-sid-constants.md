---
description: Définissez pour les fonctionnalités connues des applications à l’aide de la fonction AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes SID de capacité (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37a06c0bd0115c4f7d05753825477b5de4948d1ddb9576aea46933a63cbf409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783213"
---
# <a name="capability-sid-constants"></a>Constantes SID de capacité

Les constantes de SID de fonctionnalité définissent pour les fonctionnalités bien connues des applications à l’aide de la fonction [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**\_ \_ client Internet des fonctionnalités de sécurité \_**
</dt> <dd> <dl> <dt>

(0x00000001L)
</dt> <dt>



Un compte a accès à Internet à partir d’un ordinateur client.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**\_ \_ \_ serveur client Internet de capacité de sécurité \_**
</dt> <dd> <dl> <dt>

(0x00000002L)
</dt> <dt>



Un compte a accès à Internet à partir des ordinateurs client et serveur.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_ \_ \_ serveur client de réseau \_ privé \_ de fonctionnalités de sécurité**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Un compte a accès à Internet à partir d’un réseau privé.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_bibliothèque d' \_ images des fonctionnalités de sécurité \_**
</dt> <dd> <dl> <dt>

(0x00000004L)
</dt> <dt>



Un compte a accès à la bibliothèque d’images.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**bibliothèque de vidéos sur les fonctionnalités de sécurité \_ \_ \_**
</dt> <dd> <dl> <dt>

(0x00000005L)
</dt> <dt>



Un compte a accès à la bibliothèque vidéos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**Médiathèque sur les fonctionnalités de sécurité \_ \_ \_**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Un compte a accès à la bibliothèque musique.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**bibliothèque de documents sur les capacités de sécurité \_ \_ \_**
</dt> <dd> <dl> <dt>

(0x00000007L)
</dt> <dt>



Un compte a accès à la bibliothèque de documentation.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_authentification de \_ l’entreprise des fonctionnalités de sécurité \_**
</dt> <dd> <dl> <dt>

(0x00000008L)
</dt> <dt>



un compte a accès aux informations d’identification par défaut de Windows.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_certificats d' \_ \_ utilisateur partagé de capacité \_ de sécurité**
</dt> <dd> <dl> <dt>

(0x00000009L)
</dt> <dt>



Un compte a accès aux certificats utilisateur partagés.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ stockage amovible des fonctionnalités de sécurité \_**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Un compte a accès au stockage amovible.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Lors de la construction d’un SID de fonctionnalité, vous devez inclure l’autorité de package, l' \_ \_ \_ autorité {0,0,0,0,0,15} de package d’application de sécurité, dans l’appel à la fonction [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) . En outre, vous avez besoin du RID de base et du nombre RID pour les fonctionnalités intégrées, le RID de base des fonctionnalités de sécurité \_ \_ \_ (0x00000003L) et le \_ nombre RID de capacités builtin de sécurité \_ \_ \_ (2L).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

