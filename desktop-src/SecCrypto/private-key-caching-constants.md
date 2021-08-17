---
description: Utilisé pour représenter les entrées de Registre qui contrôlent la mise en cache de clé privée par les fournisseurs de services de chiffrement logiciels Microsoft.
ms.assetid: 67909072-72fe-4777-ae52-a7b9047c9dd5
title: Constantes de mise en cache de clé privée (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d4caf6a3973a5113e03cbe24882241609ff83b8be65a20492f8f967abb734f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978560"
---
# <a name="private-key-caching-constants"></a>Constantes de mise en cache de clés privées

Les constantes suivantes sont utilisées pour représenter les entrées de Registre qui contrôlent la mise en cache des [*clés privées*](../secgloss/p-gly.md) par les fournisseurs de services de chiffrement logiciels Microsoft.



| Constante/valeur                                                                                                                                                                                                                                                                                                                                                                                    | Description                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span id="szKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><span id="szkey_cryptoapi_private_key_options"></span><span id="SZKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><dl> <dt>**szKEY \_ \_Options de \_ clé \_ privée CryptoAPI**</dt> <dt>« stratégies logicielles de \\ \\ \\ \\ \\ \\ chiffrement Microsoft »</dt> </dl> | Chemin d’accès, sous la racine **HKEY \_ local \_ machine** , des entrées de registre de la mise en cache de clés privées.<br/> |



Les constantes suivantes sont utilisées pour identifier les valeurs de Registre qui contrôlent globalement la mise en cache des clés privées pour un processus spécifique par les fournisseurs de services de chiffrement logiciels Microsoft.



| Constante/valeur                                                                                                                                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="szPRIV_KEY_CACHE_MAX_ITEMS"></span><span id="szpriv_key_cache_max_items"></span><span id="SZPRIV_KEY_CACHE_MAX_ITEMS"></span><dl> <dt>**szPRIV \_ \_ \_ Nombre maximal d' \_ éléments de cache de clé**</dt> <dt>« PrivKeyCacheMaxItems »</dt> </dl>                                                                  | Valeur **reg \_ DWORD** sous la clé de Registre **szKEY \_ CryptoAPI \_ Private \_ Key \_ options** qui spécifie le nombre maximal de clés privées qui peuvent être mises en cache en une seule fois pour un seul processus. Cette vérification est effectuée chaque fois qu’une clé privée stockée est lue. Si le nombre maximal est dépassé, la clé la moins utilisée récemment est supprimée du cache.<br/> Si cette valeur est égale à zéro, aucune clé n’est mise en cache. Si cette valeur n’est pas présente, la valeur par défaut de l’option **\_ \_ \_ nombre maximal d' \_ \_ éléments du cache de clé cPRIV** est utilisée par défaut.<br/> Si une clé privée qui est supprimée du cache est actuellement référencée dans un contexte ouvert, la clé est lue à partir du stockage la prochaine fois qu’une tentative est effectuée pour utiliser la clé.<br/> **Windows Server 2003 et Windows XP avec SP1 et versions antérieures :** Cette valeur de Registre n’est pas prise en charge.<br/>                                  |
| <span id="cPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><span id="cpriv_key_cache_max_items_default"></span><span id="CPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><dl> <dt>**cPRIV \_ \_ \_ Nombre maximal d' \_ éléments \_ par défaut du cache de clés**</dt> <dt>20</dt> </dl>                                                         | Valeur par défaut de l’entrée de Registre **szPRIV \_ Key \_ cache \_ Max \_ Items** si aucune valeur n’est spécifiée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="szPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><span id="szpriv_key_cache_purge_interval_seconds"></span><span id="SZPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><dl> <dt>**szPRIV \_ \_Intervalle de purge du cache de clés en \_ \_ \_ secondes**</dt> <dt>« PrivKeyCachePurgeIntervalSeconds »</dt> </dl> | Valeur **reg \_ DWORD** sous la clé de Registre **szKEY \_ CryptoAPI \_ Private \_ Key \_ options** qui spécifie l’âge maximal, en secondes, de n’importe quelle clé privée mise en cache. Cette vérification est effectuée chaque fois qu’une clé privée stockée est utilisée ou lue. Si ce laps de temps s’est écoulé depuis la dernière suppression, toutes les clés mises en cache qui n’ont pas été référencées depuis la dernière suppression sont supprimées du cache.<br/> Si cette valeur n’est pas présente, la valeur **\_ \_ \_ \_ \_ \_ par défaut de l’intervalle de purge du cache de clé cPRIV** est utilisée comme valeur par défaut.<br/> Si une clé privée qui est effacée du cache est actuellement référencée dans un contexte ouvert, la clé est lue à partir du stockage la prochaine fois qu’une tentative est effectuée pour utiliser la clé.<br/> **Windows Server 2003 et Windows XP avec SP1 et versions antérieures :** Cette valeur de Registre n’est pas prise en charge.<br/> |
| <span id="cPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><span id="cpriv_key_cache_purge_interval_seconds_default"></span><span id="CPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><dl> <dt>**cPRIV \_ \_Intervalle de purge du cache de clés en \_ \_ \_ secondes \_ par défaut**</dt> <dt>86400</dt> </dl> | La valeur par défaut de l’entrée de Registre **szPRIV \_ Key \_ cache \_ intervalle de purge des \_ \_ secondes** si aucune valeur n’est spécifiée. Cette valeur est équivalente à un jour.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



Les constantes suivantes sont utilisées pour identifier les valeurs de Registre qui contrôlent la mise en cache des clés privées pour une seule instance du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) basée sur des logiciels Microsoft.



| Constante/valeur                                                                                                                                                                                                                                                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>« AllowCachePW »</dt> </dl>                                                                                                                                                         | Valeur **reg \_ DWORD** sous la clé de Registre **HKEY \_ local \_ machine \\ Software \\ Policies \\ Microsoft \\ Cryptography \\ Protect** , qui spécifie si la mise en cache de mot de passe est activée pour les clés protégées par mot de passe dans les fournisseurs de services de chiffrement logiciels Microsoft. Si cette valeur est égale à 0, la mise en cache du mot de passe est désintégrée et l’utilisateur est invité à entrer le mot de passe chaque fois qu’une clé protégée par mot de passe est utilisée. Toute autre valeur, ou l’absence de cette valeur, indique que le mot de passe sera mis en cache. Dans ce scénario, l’utilisateur n’est invité qu’une seule fois par processus pour chaque clé. <br/> |
| <span id="szKEY_CACHE_ENABLED"></span><span id="szkey_cache_enabled"></span><span id="SZKEY_CACHE_ENABLED"></span><dl> <dt>**szKEY \_ CACHE \_ activé**</dt> <dt>« CachePrivateKeys »</dt> </dl>          | Valeur **reg \_ DWORD** sous la clé de Registre **szKEY \_ CryptoAPI \_ Private \_ Key \_ options** qui spécifie si la mise en cache de la clé privée est activée. Si cette valeur est 1, la mise en cache de la clé privée est activée. Toute autre valeur, ou l’absence de cette valeur, indique que la mise en cache de la clé privée est désactivée.<br/> **Windows vista avec SP1, Windows vista et Windows XP :** Cette valeur de Registre n’est pas prise en charge.<br/>                                                                                                                                                        |
| <span id="szKEY_CACHE_SECONDS"></span><span id="szkey_cache_seconds"></span><span id="SZKEY_CACHE_SECONDS"></span><dl> <dt>**szKEY \_ \_Secondes du cache**</dt> <dt>« PrivateKeyLifetimeSeconds »</dt> </dl> | Valeur **reg \_ DWORD** sous la clé de Registre **szKEY \_ CryptoAPI \_ Private \_ Key \_ options** qui spécifie l’âge maximal, en secondes, de n’importe quelle clé privée mise en cache.<br/> **Windows XP :** Cette valeur de Registre n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Remarques

Les différences entre les **\_ \_ secondes du cache szKEY** et les valeurs de l' **\_ \_ \_ \_ intervalle de \_ purge du cache de clé szPRIV** sont les suivantes :

 **\_secondes du cache szKEY \_**  

-   Cette valeur s’applique uniquement à un CSP spécifique. Une fois le CSP libéré, le cache du CSP est également libéré.  
-   Cette valeur est appliquée uniquement lorsqu’une tentative d’utilisation d’une clé privée spécifique avec un handle de contexte spécifique est effectuée.  

**\_intervalle de \_ purge du cache de clé szPRIV en \_ \_ \_ secondes**  

-   Cette valeur s’applique à tous les fournisseurs de services de chiffrement d’un processus. Même si le CSP est publié, ce cache n’est pas libéré.  
-   Cette valeur s’applique chaque fois qu’une clé privée stockée est utilisée ou lue à partir du stockage dans un seul processus.  



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
