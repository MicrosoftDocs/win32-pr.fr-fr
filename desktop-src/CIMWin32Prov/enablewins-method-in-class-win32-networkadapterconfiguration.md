---
description: EnableWINS &\# 32 ; la méthode statique de la classe WMI active les paramètres WINS (Windows Internet Service de nommage) spécifiques à TCP/IP, mais indépendamment de la carte réseau.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Méthode EnableWINS de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ce820e515bb72cbd2521521726f2b6962c49ee1b453781b5d17993c45e0d22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676502"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode EnableWINS de la \_ classe Win32 NetworkAdapterConfiguration

la méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** permet Windows paramètres WINS (Internet Service de nommage) spécifiques à TCP/IP, mais indépendamment de la carte réseau.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DNSEnabledForWINSResolution* \[ dans\]
</dt> <dd>

Si la **valeur est true**, le système DNS (Domain Name System) est activé pour la résolution de noms sur la résolution WINS.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ dans\]
</dt> <dd>

Si la **valeur est true**, les fichiers de recherche locaux sont utilisés. Les fichiers de recherche contiendront des mappages d’adresses IP aux noms d’hôtes.

</dd> <dt>

*WINSHostLookupFile* \[ dans, facultatif\]
</dt> <dd>

Fichiers de recherche qui contiennent des mappages d’adresses IP à des noms d’hôtes. S’ils sont disponibles, les fichiers se trouvent dans% SystemRoot% \\ system32 \\ drivers \\ .

</dd> <dt>

*WINSScopeID* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’identificateur d’étendue qui sera ajoutée à la fin du nom NetBIOS de l’ordinateur. Les systèmes qui utilisent le même identificateur d’étendue peuvent communiquer avec cet ordinateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis ; 1 (un) pour une exécution réussie lorsqu’un redémarrage est nécessaire ; nombre différent en cas d’erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

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

## <a name="examples"></a>Exemples

L’exemple de code [activer WINS pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript, sur la Galerie TechNet, utilise **ENABLEWINS** pour activer WINS sur toutes les cartes réseau installées sur un ordinateur.

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

 

