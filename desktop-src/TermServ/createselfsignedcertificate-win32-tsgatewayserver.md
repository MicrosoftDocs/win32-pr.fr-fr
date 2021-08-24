---
title: Méthode CreateSelfSignedCertificate de la classe Win32_TSGatewayServer
description: Crée un certificat auto-signé et retourne le hachage du certificat en tant que \ 0034 ; out \ 0034 ; paramètre.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateSelfSignedCertificate
- Services Bureau à distance de la méthode CreateSelfSignedCertificate, classe Win32_TSGatewayServer
- Win32_TSGatewayServer de la classe Services Bureau à distance, méthode CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200b08da8d5eea9f31405a357650384081c407df4eb76820cd47a111e6b66aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139052"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Méthode CreateSelfSignedCertificate de la \_ classe Win32 TSGatewayServer

Crée un certificat auto-signé et retourne le hachage du certificat en tant que paramètre « out ». Ajoute également le texte « \_ \_ certificat auto- \_ signé de la passerelle TS \_ » à la propriété de contexte de certificat afin que le certificat soit reconnu en tant que certificat de passerelle des services Bureau à bureau à distance. Cette méthode utilise un conteneur de clé spécifique à la passerelle des services Bureau à distance pour créer le certificat.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SubjectName* \[ dans\]
</dt> <dd>

Nom du sujet du certificat auto-signé.

</dd> <dt>

*Certhash* \[ à\]
</dt> <dd>

Hachage du certificat.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServer Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 

