---
description: SetGateways &\# 32 ; La méthode de classe WMI spécifie une liste de passerelles pour le routage des paquets vers un sous-réseau différent du sous-réseau auquel la carte réseau est connectée.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Méthode SetGateways de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124042"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode SetGateways de la \_ classe Win32 NetworkAdapterConfiguration

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** spécifie une liste de passerelles pour le routage des paquets vers un sous-réseau différent du sous-réseau auquel la carte réseau est connectée.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DefaultIPGateway* \[ dans\]
</dt> <dd>

Liste des adresses IP vers les passerelles où les paquets réseau sont routés.

</dd> <dt>

*GatewayCostMetric* \[ dans, facultatif\]
</dt> <dd>

Affecte une valeur comprise entre 1 et 9999, qui est utilisée pour calculer les itinéraires les plus rapides et les plus fiables. Les valeurs de ce paramètre correspondent aux valeurs du paramètre *DefaultIPGateway* . La valeur par défaut d’une passerelle est 1.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 (zéro) pour une exécution réussie lorsqu’un redémarrage n’est pas nécessaire, 1 (un) pour une exécution réussie lorsqu’un redémarrage est requis, et toute autre valeur en cas d’erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Exécution réussie, aucun redémarrage requis**
</dt> <dd>

0

</dd> <dt>

**Achèvement réussi, redémarrage requis**
</dt> <dd>

1

</dd> <dt>

**Méthode non prise en charge sur cette plateforme**
</dt> <dd>

64

Méthode non prise en charge lorsque la carte réseau est en mode DHCP.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

65

</dd> <dt>

**Masque de sous-réseau non valide**
</dt> <dd>

66

</dd> <dt>

**Une erreur s’est produite lors du traitement d’une instance qui a été retournée**
</dt> <dd>

67

</dd> <dt>

**Paramètre d’entrée non valide**
</dt> <dd>

68

</dd> <dt>

**Plus de 5 passerelles spécifiées**
</dt> <dd>

69

</dd> <dt>

**Adresse IP non valide**
</dt> <dd>

70

</dd> <dt>

**Adresse IP de passerelle non valide**
</dt> <dd>

71

</dd> <dt>

**Une erreur s’est produite lors de l’accès au registre pour les informations demandées**
</dt> <dd>

72

</dd> <dt>

**Nom de domaine non valide**
</dt> <dd>

73

</dd> <dt>

**Nom d’hôte non valide**
</dt> <dd>

74

</dd> <dt>

**Aucun serveur WINS principal/secondaire défini**
</dt> <dd>

75

</dd> <dt>

**Fichier non valide**
</dt> <dd>

76

</dd> <dt>

**Chemin système non valide**
</dt> <dd>

77

</dd> <dt>

**Échec de la copie du fichier**
</dt> <dd>

78

</dd> <dt>

**Paramètre de sécurité non valide**
</dt> <dd>

79

</dd> <dt>

**Impossible de configurer le service TCP/IP**
</dt> <dd>

80

</dd> <dt>

**Impossible de configurer le service DHCP**
</dt> <dd>

81

</dd> <dt>

**Impossible de renouveler le bail DHCP**
</dt> <dd>

82

</dd> <dt>

**Impossible de libérer le bail DHCP**
</dt> <dd>

83

</dd> <dt>

**IP non activé sur l’adaptateur**
</dt> <dd>

84

</dd> <dt>

**IPX non activé sur l’adaptateur**
</dt> <dd>

85 %

</dd> <dt>

**Erreur liée à un nombre de trames/réseau**
</dt> <dd>

86

</dd> <dt>

**Type de trame non valide**
</dt> <dd>

87

</dd> <dt>

**Numéro de réseau non valide**
</dt> <dd>

88

</dd> <dt>

**Numéro de réseau en double**
</dt> <dd>

89

</dd> <dt>

**Paramètre hors limites**
</dt> <dd>

90

</dd> <dt>

**Accès refusé**
</dt> <dd>

91

</dd> <dt>

**Mémoire insuffisante**
</dt> <dd>

92

</dd> <dt>

**Existe déjà**
</dt> <dd>

93

</dd> <dt>

**Chemin d’accès, fichier ou objet introuvable**
</dt> <dd>

94

</dd> <dt>

**Impossible de notifier le service**
</dt> <dd>

95

</dd> <dt>

**Impossible d’informer le service DNS**
</dt> <dd>

96

</dd> <dt>

**Interface non configurable**
</dt> <dd>

97

</dd> <dt>

**Tous les baux DHCP n’ont pas pu être libérés/renouvelés**
</dt> <dd>

98

</dd> <dt>

**DHCP n’est pas activé sur l’adaptateur**
</dt> <dd>

100

</dd> <dt>

**Autres**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Notes

Cette méthode fonctionne uniquement lorsque la carte d’interface réseau (NIC) est en mode IP statique.

Pour effacer la passerelle, définissez votre passerelle sur la même adresse IP que celle que vous utilisez sur [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).

## <a name="examples"></a>Exemples

L’exemple de [modification de passerelles pour une carte réseau](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) configure deux passerelles pour une carte réseau.

L’exemple VBScript [attribuer une adresse IP statique](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) définit l’adresse IP et la passerelle d’un ordinateur.

L' [adresse IP statique, puis la jointure à un](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) exemple PowerShell de domaine facilite la reconstruction des machines.

## <a name="requirements"></a>Spécifications



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

 

