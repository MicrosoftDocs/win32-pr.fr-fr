---
description: SetDNSServerSearchOrder &\# 32 ; La méthode de classe WMI utilise un tableau d’éléments de chaîne pour définir l’ordre de recherche du serveur.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Méthode SetDNSServerSearchOrder de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ae53996e2f8199d552909a186ab17e6b7ec89857c9be24dc4d8d4bfe583cfea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759799"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode SetDNSServerSearchOrder de la \_ classe Win32 NetworkAdapterConfiguration

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** utilise un tableau d’éléments de chaîne pour définir l’ordre de recherche du serveur.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DNSServerSearchOrder* \[ dans\]
</dt> <dd>

Liste des adresses IP de serveur à interroger pour les serveurs DNS.

Exemple : 130.215.24.1 ou 157.54.164.1

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

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

**Autre** (101 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarques

Il s’agit d’un appel de méthode dépendant de l’instance qui s’applique sur la base de chaque adaptateur. Une fois que les serveurs DNS statiques sont spécifiés pour commencer à utiliser le protocole DHCP (Dynamic Host Configuration Protocol) au lieu de serveurs DNS statiques, vous pouvez appeler la méthode sans fournir de paramètres « in ».

## <a name="examples"></a>Exemples

L’exemple de [commande définir l’ordre de recherche des serveurs DNS pour plusieurs ordinateurs dans une unité d’organisation](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) dans la Galerie TechNet récupère ou définit l’ordre de recherche des serveurs DNS pour plusieurs ordinateurs appartenant à une unité d’organisation.

L’exemple de [modification de l’ordre de recherche d’un serveur DNS pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) configure une carte réseau TCP/IP pour utiliser deux serveurs DNS.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tâches WMI : mise en réseau](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tâches WMI : comptes et domaines](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Prise en charge D’ipv6 et IPv6 dans WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

