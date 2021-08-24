---
description: définit Exchange le numéro de réseau virtuel (IPX) du réseau virtuel sur le système de l’ordinateur cible.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Méthode SetIPXVirtualNetworkNumber de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: 37af763450eab2fdba373fe21bfde5c0b4e1e38fda1f42aff59c425ba6b10000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079773"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode SetIPXVirtualNetworkNumber de la \_ classe Win32 NetworkAdapterConfiguration

définit Exchange le numéro de réseau virtuel (IPX) du réseau virtuel sur le système de l’ordinateur cible. Windows 2000 et Windows NT 3,51 ou version ultérieure utilise un numéro de réseau interne pour le routage interne. Le numéro de réseau interne est également appelé « numéro de réseau virtuel ». Il identifie de façon unique le système informatique sur le réseau. La méthode retourne une valeur entière qui peut être interprétée comme suit :

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IPXVirtualNetNumber* \[ dans\]
</dt> <dd>

Numéro de réseau virtuel pour ce système.

</dd> </dl>

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

 

 




