---
description: La méthode de classe WMI RenewDHCPLease renouvelle l’adresse IP sur des cartes réseau compatibles DHCP spécifiques.
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Méthode RenewDHCPLease de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033784"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode RenewDHCPLease de la \_ classe Win32 NetworkAdapterConfiguration

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLease** renouvelle l’adresse IP sur des cartes réseau compatibles DHCP spécifiques.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) pour une exécution réussie quand aucun redémarrage n’est requis, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et un autre nombre en cas d’erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Exécution réussie, aucun redémarrage requis**
</dt> <dd>

0

Opération réussie, aucun redémarrage n’est nécessaire.

</dd> <dt>

**Achèvement réussi, redémarrage requis**
</dt> <dd>

1

Opération terminée, redémarrage requis.

</dd> <dt>

**Méthode non prise en charge sur cette plateforme**
</dt> <dd>

64

Méthode non prise en charge sur cette plateforme.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

65

Échec inconnu.

</dd> <dt>

**Masque de sous-réseau non valide**
</dt> <dd>

66

Masque de sous-réseau non valide.

</dd> <dt>

**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**
</dt> <dd>

67

Une erreur s’est produite lors du traitement d’une instance qui a été retournée.

</dd> <dt>

**Paramètre d’entrée non valide**
</dt> <dd>

68

Paramètre d’entrée non valide.

</dd> <dt>

**Plus de 5 passerelles spécifiées**
</dt> <dd>

69

Plus de cinq passerelles sont spécifiées.

</dd> <dt>

**Adresse IP non valide**
</dt> <dd>

70

Adresse IP non valide.

</dd> <dt>

**Adresse IP de passerelle non valide**
</dt> <dd>

71

Adresse IP de passerelle non valide.

</dd> <dt>

**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**
</dt> <dd>

72

Une erreur s’est produite lors de l’accès au registre pour les informations demandées.

</dd> <dt>

**Nom de domaine non valide**
</dt> <dd>

73

Nom de domaine non valide.

</dd> <dt>

**Nom d’hôte non valide**
</dt> <dd>

74

Nom d’hôte non valide.

</dd> <dt>

**Aucun serveur WINS principal/secondaire défini**
</dt> <dd>

75

Aucun serveur WINS principal ou secondaire n’est défini.

</dd> <dt>

**Fichier non valide**
</dt> <dd>

76

Fichier non valide.

</dd> <dt>

**Chemin système non valide**
</dt> <dd>

77

Chemin d’accès système non valide.

</dd> <dt>

**Échec de la copie du fichier**
</dt> <dd>

78

Échec de la copie du fichier.

</dd> <dt>

**Paramètre de sécurité non valide**
</dt> <dd>

79

Paramètre de sécurité non valide.

</dd> <dt>

**Impossible de configurer le service TCP/IP**
</dt> <dd>

80

Impossible de configurer le service TCP/IP.

</dd> <dt>

**Impossible de configurer le service DHCP**
</dt> <dd>

81

Impossible de configurer le service DHCP.

</dd> <dt>

**Impossible de renouveler le bail DHCP**
</dt> <dd>

82

Impossible de renouveler le bail DHCP.

</dd> <dt>

**Impossible de libérer le bail DHCP**
</dt> <dd>

83

Impossible de libérer le bail DHCP.

</dd> <dt>

**IP non activé sur l’adaptateur**
</dt> <dd>

84

IP non activé sur l’adaptateur.

</dd> <dt>

**IPX non activé sur l’adaptateur**
</dt> <dd>

85 %

IPX n’est pas activé sur l’adaptateur.

</dd> <dt>

**Erreur liée à un nombre de trames/réseau**
</dt> <dd>

86

Erreur liée à l’image ou au numéro de réseau.

</dd> <dt>

**Type de trame non valide**
</dt> <dd>

87

Type de trame non valide.

</dd> <dt>

**Numéro de réseau non valide**
</dt> <dd>

88

Numéro de réseau non valide.

</dd> <dt>

**Numéro de réseau en double**
</dt> <dd>

89

Numéro de réseau en double.

</dd> <dt>

**Paramètre hors limites**
</dt> <dd>

90

Paramètre hors limites.

</dd> <dt>

**Accès refusé**
</dt> <dd>

91

Accès refusé.

</dd> <dt>

**Mémoire insuffisante**
</dt> <dd>

92

Mémoire insuffisante.

</dd> <dt>

**Existe déjà**
</dt> <dd>

93

Existe déjà.

</dd> <dt>

**Chemin d’accès, fichier ou objet introuvable**
</dt> <dd>

94

Chemin d’accès, fichier ou objet introuvable.

</dd> <dt>

**Impossible de notifier le service**
</dt> <dd>

95

Impossible de notifier le service.

</dd> <dt>

**Impossible d’informer le service DNS**
</dt> <dd>

96

Impossible d’informer le service DNS.

</dd> <dt>

**Interface non configurable**
</dt> <dd>

97

Interface non configurable.

</dd> <dt>

**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**
</dt> <dd>

98

Tous les baux DHCP n’ont pas pu être libérés ou renouvelés.

</dd> <dt>

**DHCP n’est pas activé sur l’adaptateur**
</dt> <dd>

100

DHCP n’est pas activé sur l’adaptateur.

</dd> <dt>

**Autres**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Notes

Le bail de l’adresse IP attribuée par un serveur DHCP a une date d’expiration que le client doit renouveler s’il a l’intention de continuer à utiliser l’adresse IP attribuée.

## <a name="examples"></a>Exemples

La [version renouveler les adresses IP à l’aide](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) de PowerShell PowerShell dans la Galerie TechNet utilise **RenewDHCPLease** pour publier et renouveler une adresse IP.

L’exemple de [renouvellement de bail DHCP pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) dans la Galerie TechNet utilise **RenewDHCPLease** pour renouveler le bail DHCP pour chaque carte réseau TCP/IP d’un ordinateur.

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

 

