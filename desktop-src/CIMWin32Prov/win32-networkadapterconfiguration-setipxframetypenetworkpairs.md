---
description: définit le numéro de réseau ou les paires de trames (IPX) de Exchange de paquets interréseau pour cette carte réseau.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Méthode SetIPXFrameTypeNetworkPairs de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: f914f996e26d64ae66c0be2acf1dee3988ccc2015109c6e7d3b340b406c0c23e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973023"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode SetIPXFrameTypeNetworkPairs de la \_ classe Win32 NetworkAdapterConfiguration

définit le numéro de réseau ou les paires de trames (IPX) de Exchange de paquets interréseau pour cette carte réseau.

Windows 2000 et Windows NT 3,51 et versions ultérieures utilisent un numéro de réseau IPX à des fins de routage. Elle est affectée à chaque combinaison de type de trame/carte réseau configurée sur votre système informatique. Ce nombre est parfois appelé « numéro de réseau externe ». Elle doit être unique pour chaque segment de réseau. Si le type de trame est défini sur AUTO, le numéro de réseau doit être égal à zéro.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IPXNetworkNumber* \[ dans\]
</dt> <dd>

Tableau de caractères qui identifient de façon unique un adaptateur sur le système informatique. le transport compatible IPX/SPX NetWare Link (NWLink) dans Windows 2000 et Windows NT 3,51 ou version ultérieure utilise deux types différents de numéros de réseau. Ce nombre est parfois appelé numéro de réseau externe. Elle doit être unique pour chaque segment de réseau. Les valeurs de cette liste de chaînes doivent avoir une valeur correspondante dans le paramètre IPXFrameType identifiant le type de trame de paquet utilisé pour ce réseau.

</dd> <dt>

*IPXFrameType* \[ dans\]
</dt> <dd>

Tableau d’entiers des identificateurs de type de frame. Les valeurs de ce tableau correspondent aux éléments dans le paramètre *IPXNetworkNumber* .

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Snap Ethernet** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Automatique** (255)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

<dl> <dt>

**Exécution réussie, aucun redémarrage requis** (0)
</dt> <dt>

**Achèvement réussi, redémarrage requis** (1)
</dt> <dt>

**Méthode non prise en charge sur cette plateforme** (64)
</dt> <dt>

**Échec inconnu** (65)
</dt> <dt>

**Masque de sous-réseau non valide** (66)
</dt> <dt>

**Une erreur s’est produite lors du traitement d’une instance qui a été retournée** (67)
</dt> <dt>

**Paramètre d’entrée non valide** (68)
</dt> <dt>

**Plus de 5 passerelles spécifiées** (69)
</dt> <dt>

**Adresse IP non valide** (70)
</dt> <dt>

**Adresse IP de passerelle non valide** (71)
</dt> <dt>

**Une erreur s’est produite lors de l’accès au registre pour les informations demandées** (72)
</dt> <dt>

**Nom de domaine non valide** (73)
</dt> <dt>

**Nom d’hôte non valide** (74)
</dt> <dt>

**Aucun serveur WINS principal/secondaire défini** (75)
</dt> <dt>

**Fichier non valide** (76)
</dt> <dt>

**Chemin système non valide** (77)
</dt> <dt>

**Échec** de la copie du fichier (78)
</dt> <dt>

**Paramètre de sécurité non valide** (79)
</dt> <dt>

**Impossible de configurer le service TCP/IP** (80)
</dt> <dt>

**Impossible de configurer le service DHCP** (81)
</dt> <dt>

**Impossible de renouveler le bail DHCP** (82)
</dt> <dt>

**Impossible de libérer le bail DHCP** (83)
</dt> <dt>

**IP non activé sur l’adaptateur** (84)
</dt> <dt>

**IPX non activé sur l’adaptateur** (85)
</dt> <dt>

**Erreur liée à un nombre de trames/réseau** (86)
</dt> <dt>

**Type de trame non valide** (87)
</dt> <dt>

**Numéro de réseau non valide** (88)
</dt> <dt>

**Numéro de réseau en double** (89)
</dt> <dt>

**Paramètre hors limites** (90)
</dt> <dt>

**Accès refusé** (91)
</dt> <dt>

**Mémoire insuffisante** (92)
</dt> <dt>

**Existe déjà** (93)
</dt> <dt>

**Chemin d’accès, fichier ou objet introuvable** (94)
</dt> <dt>

**Impossible de notifier le service** (95)
</dt> <dt>

**Impossible d’informer le service DNS** (96)
</dt> <dt>

**Interface non configurable** (97)
</dt> <dt>

**Tous les baux DHCP n’ont pas pu être libérés/renouvelés** (98)
</dt> <dt>

**DHCP n’est pas activé sur la carte** (100)
</dt> <dt>

**Autre** (101 à 4294967295)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




