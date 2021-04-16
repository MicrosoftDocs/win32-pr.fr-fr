---
description: Contient des informations détaillées sur une interface requise par un client RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: Structure INTF_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527651"
---
# <a name="intf_entry-structure"></a>\_Structure d’entrée INTF

\[**INTF \_ L’entrée** n’est plus prise en charge à partir de Windows Vista et Windows Server 2008. Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires. Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

Contient des informations détaillées sur une interface requise par un client RPC.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**wszGuid**
</dt> <dd>

Pointeur vers le GUID d’interface représenté sous la forme d’une chaîne Unicode au format suivant : "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> <dt>

**wszDescr**
</dt> <dd>

Pointeur vers une chaîne qui contient la description d’interface récupérée par le service de configuration automatique sans fil (WZCSVC).

</dd> <dt>

**dwContext**
</dt> <dd>

Réservé à un usage interne.

</dd> <dt>

**ulMediaState**
</dt> <dd>

État de connexion du média NDIS actuel pour l’interface. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                                  | Signification                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <dt> **État du support \_ \_ connecté**</dt> <dt>1</dt> </dl>       | Le média est connecté.<br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <dt>**Éléments multimédias \_ ÉTAT \_ déconnecté**</dt> <dt>0</dt> </dl> | Le média est déconnecté.<br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <dt>**Éléments multimédias \_ ÉTAT \_ inconnu**</dt> <dt>-1</dt> </dl>               | L’état du support est inconnu.<br/> |



 

</dd> <dt>

**ulMediaType**
</dt> <dd>

Types de média NDIS que la carte réseau utilise actuellement. Lorsqu’il est interrogé, la valeur de ce membre est **NdisMedium802 \_ 3** , comme défini dans le fichier d’en-tête *Ndispnp. h* .

</dd> <dt>

**ulPhysicalMediaType**
</dt> <dd>

Type de média NDIS pour l’interface. Lors de la requête, la valeur de ce membre est **NdisPhysicalMediumWirelessLan** comme défini dans le fichier d’en-tête *Ndispnp. h* .

</dd> <dt>

**nInfraMode**
</dt> <dd>

Mode d’infrastructure actuel 802,11 défini sur l’interface.

</dd> <dt>

**nAuthMode**
</dt> <dd>

Mode d’authentification 802,11 actuel défini sur l’interface.

Le tableau suivant indique les valeurs possibles pour le paramètre en fonction de l’énumération du **\_ \_ \_ \_ mode d’authentification NDIS 802 11** définie dans le fichier d’en-tête *NtDDNdis. h* .



| Valeur                                                                                                                                                                                                                                                                                                            | Signification                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt> </dl>                         | Authentification système Open IEEE 802,11.<br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt> </dl>                 | Authentification partagée IEEE 802,11 qui utilise une clé WEP (Wired Equivalent Privacy) prépartagée. <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt> </dl> | Mode de basculement automatique. Lorsque vous utilisez le mode de basculement automatique, la carte d’interface réseau (NIC) sans fil tente d’abord d’utiliser le mode d’authentification partagé. Si le mode partagé échoue, la carte réseau tente d’utiliser le mode d’authentification ouvert. <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt> </dl>                             | Sécurité WPA (Wireless Protected Access). L’authentification est effectuée entre le demandeur, l’authentificateur et le serveur d’authentification sur IEEE 802.1 X. Les clés de chiffrement sont dynamiques et sont dérivées par le processus d’authentification. <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt> </dl>                 | La sécurité WPA à l’aide d’une clé prépartagée. L’authentification est effectuée entre le demandeur et l’authentificateur sur IEEE 802.1 X. Les clés de chiffrement sont dynamiques et sont dérivées de la clé prépartagée utilisée par le demandeur et l’authentificateur. <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt> </dl>             | Sécurité WPA. L’authentification s’effectue à l’aide d’une clé prépartagée sans authentification IEEE 802.1 X. Les clés de chiffrement sont statiques et sont dérivées de la clé prépartagée. Ce mode s’applique uniquement aux types de réseau ad hoc. <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt> </dl>                         | Sécurité WPA2. L’authentification est effectuée entre le demandeur, l’authentificateur et le serveur d’authentification sur IEEE 802.1 X. Les clés de chiffrement sont dynamiques et sont dérivées par le processus d’authentification. <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt> </dl>             | Spécifie la sécurité WPA2. L’authentification est effectuée entre le demandeur et l’authentificateur sur IEEE 802 1X. Les clés de chiffrement sont dynamiques et sont dérivées de la clé prépartagée utilisée par le demandeur et l’authentificateur. <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt> </dl>                             | Valeur maximale possible pour la valeur d’énumération du **\_ \_ \_ \_ mode d’authentification NDIS 802 11** . Il ne s’agit pas d’une valeur légale pour le mode d’authentification. <br/>                                                                                        |



 

</dd> <dt>

**nWepStatus**
</dt> <dd>

Mode de chiffrement actuel 802,11 défini sur l’interface.

</dd> <dt>

**dwCtlFlags**
</dt> <dd>

Valeur de masque de masque des indicateurs de contrôle qui indiquent la manière dont WZCSVC fonctionne sur l’interface.

Le tableau suivant indique les valeurs de bit possibles.



| Valeur                                                                                                                                                                                                                                 | Signification                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <dt>**INTFCTL \_ 0x0007 \_ masque de cm**</dt> <dt></dt> </dl>      | Masque de masque pour le mode de filtre réseau. INTFCTL \_ cm \_ Mask & dwCtlFlags génère une valeur de type NDIS \_ 802 \_ 11 \_ \_ infrastructure réseau. La valeur obtenue indique si WZCSVC se connecte uniquement aux réseaux d’infrastructure, aux réseaux ad hoc ou aux deux types de réseaux.<br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <dt>**INTFCTL \_ ACTIVÉ**</dt> <dt>0x8000</dt> </dl>       | Indique si WZCSVC doit configurer l’interface.<br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <dt>**INTFCTL \_**</dt> <dt>0X4000</dt> de secours </dl>    | Si un réseau préféré n’est pas disponible, cette valeur indique si la configuration de la carte réseau doit être automatiquement configurée pour s’associer à un réseau disponible.<br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt> </dl> | Indique si le pilote de carte réseau prend en charge tous les 802,11 OID requis par WZCSVC pour fonctionner.<br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <dt> **INTFCTL \_ volatile**</dt> <dt>0x1000</dt> </dl> | Indique si les paramètres de service de cette interface doivent être conservés dans le registre. <br/> Si cette valeur est définie, ces paramètres sont volatiles et ne doivent pas être conservés dans le registre.<br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <dt> **\_ Stratégie INTFCTL**</dt> <dt>0x0800</dt> </dl>       | Indique si les paramètres de service pour cette interface font l’objet d’un push par une stratégie de groupe.<br/> Si cette valeur est définie, les paramètres du service sont envoyés à l’ordinateur local par la stratégie de groupe.<br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt> </dl> | Indique si la prise en charge de 802.1 X est activée.<br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

**dwDynFlags**
</dt> <dd>

Masque de bits des indicateurs dynamiques qui contrôlent le comportement dynamique (non persistant et non statique) sur l’interface.

Ces bits sont utiles pour déclencher des modifications dynamiques et temporaires dans la façon dont le WZCSVC agit sur l’interface. Aucun de ces bits n’étant conservé dans le registre, les paramètres ne survivront pas au redémarrage du système ou à la désactivation de l’appareil et à l’activation de la séquence.

Le tableau suivant indique les valeurs de bit possibles.



| Valeur                                                                                                                                                                                                                            | Signification                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <dt>**INTFDYN \_ Noscan**</dt> <dt>0x00000001</dt> </dl> | Indique que le WZCSVC ne doit pas demander que l’interface exécute une analyse active, mais utilise à la place les valeurs mises en cache dans le pilote de carte réseau.<br/> |



 

</dd> <dt>

**dwCapabilities**
</dt> <dd>

Spécifie les fonctionnalités du pilote.



| Valeur                                                                                                                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <dt>**INTFCAP \_ 0x000000FF \_ \_ masque de CHIFFREment Max**</dt> <dt></dt> </dl> | Les bits d’ordre inférieur de ce membre sont utilisés pour indiquer le chiffrement maximal pris en charge. Les valeurs possibles sont certaines des valeurs d’énumération définies dans la structure d' **\_ état NDIS 802 \_ 11 \_ WEP \_** dans le fichier d’en-tête *NtDDNdis. h* inclus dans le SDK Windows.<br/> La \_ valeur Ndis802 11Encryption1Enabled (2) indique que le chiffrement WEP est pris en charge. TKIP et AES ne sont pas pris en charge, et une clé de transmission peut être ou non disponible. <br/> La \_ valeur Ndis802 11Encryption2Enabled (9) indique que le protocole TKIP et le chiffrement WEP sont pris en charge. AES n’est pas pris en charge et une clé de transmission est disponible. <br/> La \_ valeur de 11Encryption3Enabled Ndis802 (11) indique que AES, TKIP et WEP sont pris en charge, et une clé de transmission est disponible. <br/> Le Ndis802 \_ 11EncryptionNotSupported (8) indique que la clé WEP n’est pas prise en charge. <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <dt>**INTFCAP \_**</dt> <dt>0x00000100</dt> SSN </dl>                                       | Indique la prise en charge d’un réseau sécurisé simple (SSN) qui est un sous-ensemble de 802.11 i. <br/> SSN modifie régulièrement la clé de chiffrement, au lieu de la norme WEP (Wired Equivalent Privacy), qui utilise une clé statique. Pour que SSN fonctionne, le chiffrement maximal pris en charge doit être au moins TKIP. Le numéro de sécurité sociale a été développé par un consortium de fournisseurs dans 2002 en tant qu’approche temporaire pour améliorer la sécurité des réseaux locaux sans fil pendant la réalisation de la norme IEEE 802.11 i.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt> </dl>                              | Indique la prise en charge de la norme IEEE 802.11 i.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

**rdNicCapabilities**
</dt> <dd>

Ensemble de fonctionnalités pour 802.11 i.

La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdNicCapabilities** quand elles sont appelées avec l’indicateur de **\_ fonctionnalités INTF** passé dans le paramètre *dwInflags* . Si l’appel de fonction réussit, le membre **pData** de la structure de **\_ données brutes** contient une structure de **\_ \_ capacité INTF 80211** .

</dd> <dt>

**rdSSID**
</dt> <dd>

Données binaires contenant le SSID 802,11 actuellement configuré sur l’interface.

La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdSSID** quand elles sont appelées avec l’indicateur **\_ SSID INTF** passé dans le paramètre *dwInflags* . Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient le membre **SsidLength** d’une structure de **\_ SSID NDIS 802 \_ \_ 11** et le membre **pData** de la structure de **\_ données brutes** contient le membre **SSID** d’une structure **NDIS \_ 802 \_ 11 \_ SSID** .

La structure du **\_ \_ \_ SSID NDIS 802 11** est définie dans le fichier d’en-tête *Ntddndis. h* .

</dd> <dt>

**rdBSSID**
</dt> <dd>

Données binaires contenant l' 802,11 BSSID configuré sur l’interface.

La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdBSSID** quand elles sont appelées avec l’indicateur **INTF \_ BSSID** passé dans le paramètre *dwInflags* . Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient la taille d’une structure d' **\_ \_ \_ \_ adresse Mac NDIS 802 11** et le membre **pData** de la structure de **\_ données brutes** contient la structure d' **\_ \_ \_ \_ adresse Mac NDIS 802 11** .

La structure d' **\_ \_ \_ \_ adresse Mac NDIS 802 11** est définie dans le fichier d’en-tête *Ntddndis. h* .

</dd> <dt>

**rdBSSIDList**
</dt> <dd>

Données binaires qui contiennent la liste des BSSIDs qui ont été récupérées pour la dernière fois par WZCSVC.

La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdBSSIDList** quand elles sont appelées avec l’indicateur **INTF \_ BSSIDLIST** passé dans le paramètre *dwInflags* . Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient la longueur de la mémoire tampon avec les données retournées et le membre **PData** de la structure de **\_ données brutes** contient la structure de liste de **\_ configuration WZC 802 \_ 11 \_ \_** .

</dd> <dt>

**rdStSSIDList**
</dt> <dd>

Données binaires qui contiennent la liste des réseaux préférés configurés pour cette interface.

La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdStSSIDList** quand elles sont appelées avec l’indicateur **INTF \_ PREFLIST** passé dans le paramètre *dwInflags* . Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient la longueur de la mémoire tampon avec les données retournées et le membre **PData** de la structure de **\_ données brutes** contient la structure de liste de **\_ configuration WZC 802 \_ 11 \_ \_** .

Si l’un des réseaux préférés est actuellement connecté, le jeu de bits **WZCCTL \_ Media \_ Connected** (0x0400) est défini pour le membre **dwCtlFlags** de la structure de **\_ \_ configuration WLAN WZC** pour le réseau.

</dd> <dt>

**rdCtrlData**
</dt> <dd>

Données binaires utilisées avec d’autres indicateurs de contrôle lors de la définition de paramètres supplémentaires sur l’interface.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure d' **\_ entrée INTF** est utilisée par les fonctions [**WZCQueryInterface**](wzcqueryinterface.md) et [**WZCRefreshInterface**](wzcrefreshinterface.md) .

La structure des **\_ données brutes** est définie comme suit :


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



Le membre *pData* pointe vers les données binaires. *DwDataLen* indique le nombre d’octets pointés par *pData*.

> [!Note]  
> Le fichier d’en-tête *wzcsapi. h* n’est pas disponible dans le SDK Windows.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP avec SP3<br/>                                                       |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 




