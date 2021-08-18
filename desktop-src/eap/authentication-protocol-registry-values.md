---
title: Valeurs de Registre du protocole d’authentification
description: Le logiciel d’installation de la DLL EAP peut créer les valeurs de Registre suivantes sous eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0822e7abb62aad136a3abbe36ee92f5b6f1ec9fbeabd6426c039f05c1f752d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739559"
---
# <a name="authentication-protocol-registry-values"></a>Valeurs de Registre du protocole d’authentification

Le logiciel d’installation de la DLL EAP peut créer les valeurs de Registre suivantes sous **&lt; eaptypeid &gt;**. Ces valeurs de Registre sont définies dans le fichier d’en-tête Raseapif. h. Les valeurs **RAS_EAP_VALUENAME_PATH** et **RAS_EAP_VALUENAME_FRIENDLY_NAME** sont requises. Le logiciel d’installation peut également créer d’autres clés et valeurs. Ils peuvent être utilisés par le protocole d’authentification lui-même. Pour plus d’informations et pour obtenir un exemple de configuration du Registre, consultez [exemple de valeurs de Registre](registry-values-example.md).

[RAS_EAP_VALUENAME_PATH](#ras_eap_valuename_path)

[RAS_EAP_VALUENAME_FRIENDLY_NAME](#ras_eap_valuename_friendly_name)

[RAS_EAP_VALUENAME_CONFIGUI](#ras_eap_valuename_configui)

[RAS_EAP_VALUENAME_DEFAULT_DATA](#ras_eap_valuename_default_data)

[RAS_EAP_VALUENAME_REQUIRE_CONFIGUI](#ras_eap_valuename_require_configui)

[RAS_EAP_VALUENAME_CONFIG_CLSID](#ras_eap_valuename_config_clsid)

[RAS_EAP_VALUENAME_IDENTITY](#ras_eap_valuename_identity)

[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Cliqu

[RAS_EAP_VALUENAME_INVOKE_NAMEDLG](#ras_eap_valuename_invoke_namedlg)

[RAS_EAP_VALUENAME_INVOKE_PWDDLG](#ras_eap_valuename_invoke_pwddlg)

[RAS_EAP_VALUENAME_ENCRYPTION](#ras_eap_valuename_encryption)

[RAS_EAP_VALUENAME_STANDALONE_SUPPORTED](#ras_eap_valuename_standalone_supported)

[RAS_EAP_VALUENAME_ROLES_SUPPORTED](#ras_eap_valuename_roles_supported)

[RAS_EAP_VALUENAME_PER_POLICY_CONFIG](#ras_eap_valuename_per_policy_config)

[RAS_EAP_VALUENAME_ISTUNNEL_METHOD](#ras_eap_valuename_istunnel_method)

[RAS_EAP_VALUENAME_FILTER_INNERMETHODS](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a>RAS_EAP_VALUENAME_PATH

| Valeur constante | Path                               |
|----------------|------------------------------------|
| Type           | REG_EXPAND_SZ                    |
| Description    | Spécifie le chemin d’accès à la DLL EAP. |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| Valeur constante | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_SZ                                                                                                                                                           |
| Description    | Spécifie un nom convivial pour le protocole d’authentification. Ce nom s’affiche dans l’interface utilisateur de l’application EAP pour les implémentations d’accès à distance et sans fil. |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| Valeur constante | ConfigUIPath                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_EXPAND_SZ                                                                                                                   |
| Description    | Spécifie le chemin d’accès à la DLL qui implémente l’interface utilisateur de configuration sur le client, car cette interface utilisateur est destinée au client uniquement. |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| Valeur constante | ConfigData                                                            |
|----------------|-----------------------------------------------------------------------|
| Type           | REG_BINARY                                                           |
| Description    | Spécifie les données de configuration par défaut pour le protocole d’authentification. |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| Valeur constante | RequireConfigUI                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_DWORD                                                                                                                                                                                                                                               |
| Description    | Spécifie si l’utilisateur doit fournir des données de configuration dans l’interface utilisateur de l’application cliente EAP. Si cette valeur est 1, l’utilisateur n’est pas autorisé à quitter l’interface utilisateur de l’application cliente EAP sans fournir de données de configuration. La valeur par défaut est 0. |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| Valeur constante | ConfigCLSID                                                   |
|----------------|---------------------------------------------------------------|
| Type           | REG_SZ                                                       |
| Description    | Spécifie l’ID de classe de l’interface utilisateur de configuration sur le serveur. |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| Valeur constante | IdentityPath                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_EXPAND_SZ                                                                                                                        |
| Description    | Spécifie le chemin d’accès à la DLL qui implémente les fonctions pour obtenir l’identité de l’utilisateur sur le client, car cette interface utilisateur est destinée au client uniquement. |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| Valeur constante | InteractiveUIPath                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_EXPAND_SZ                                                                                                                 |
| Description    | Spécifie le chemin d’accès à la DLL qui implémente l’interface utilisateur interactive sur le client, car cette interface utilisateur est destinée au client uniquement. |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| Valeur constante | InvokeUsernameDialog                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_DWORD                                                                                                                                                                                             |
| Description    | spécifie si RAS doit afficher la boîte de dialogue nom d’utilisateur standard Windows NT/Windows 2000 (valeur 1) ou appeler [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valeur 0). La valeur par défaut est 1. |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| Valeur constante | InvokePasswordDialog                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_DWORD                                                                                                                                                                                  |
| Description    | spécifie si RAS doit afficher la boîte de dialogue de mot de passe Windows NT/Windows 2000 standard. Si cette valeur existe et qu’elle est égale à 0, RAS n’affiche pas la boîte de dialogue de mot de passe. La valeur par défaut est 1. |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| Valeur constante | MPPEEncryptionSupported                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_DWORD                                                                                                                                                                                    |
| Description    | Si cette valeur est 1, le protocole d’authentification peut générer des clés pour le style de chiffrement MPPE (Microsoft Point-to-Point Encryption). Les valeurs possibles sont 0 ou 1. La valeur par défaut est 0. |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| Valeur constante | StandaloneSupported                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_DWORD                                                                                                                                                                     |
| Description    | spécifie si ce protocole d’authentification est pris en charge sur un serveur Windows 2000 autonome. La valeur 0 indique que le protocole EAP n’est pas pris en charge. La valeur par défaut est 1. |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| Valeur constante | RolesSupported                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG_DWORD                                                                                                                                                                                                                                 |
| Description    | Spécifie les différents rôles pris en charge par EAP. Cela indique s’il peut être utilisé sur un serveur ou un client, s’il est pris en charge pour les connexions RAS (VPN) ou PEAP. Le comportement par défaut consiste à afficher la méthode EAP dans PEAP et dans EAP. |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| Valeur constante | PerPolicyConfig |
|----------------|-----------------|
| Type           | REG_DWORD      |
| Description    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

Cette valeur de Registre n’est pas utilisée.

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

Cette valeur de Registre n’est pas utilisée.

