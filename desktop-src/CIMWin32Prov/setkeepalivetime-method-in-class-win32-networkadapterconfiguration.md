---
description: La méthode statique de la classe WMI SetKeepAliveTime permet de définir la fréquence à laquelle TCP tente de vérifier qu’une connexion inactive est toujours disponible en envoyant un paquet Keep Alive.
ms.assetid: 8640b109-928b-46fc-8dce-9ee5dcbd94e3
ms.tgt_platform: multiple
title: Méthode SetKeepAliveTime de la classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dc2674f3c09626749b4c7ac6151349401670e27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544584"
---
# <a name="setkeepalivetime-method-of-the-win32_networkadapterconfiguration-class"></a>Méthode SetKeepAliveTime de la \_ classe Win32 NetworkAdapterConfiguration

La méthode statique de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetKeepAliveTime** permet de définir la fréquence à laquelle TCP tente de vérifier qu’une connexion inactive est toujours disponible en envoyant un paquet Keep Alive.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetKeepAliveTime(
  [in] uint32 KeepAliveTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*KeepAliveTime* \[ dans\]
</dt> <dd>

Intervalle, en millisecondes, que le protocole TCP attend pour vérifier qu’une connexion inactive est toujours disponible.

</dd> </dl>

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

Si le système distant est toujours accessible et fonctionne, il accuse réception de la transmission Keep Alive. Les paquets Keep Alive ne sont pas envoyés par défaut. Cette fonctionnalité peut être activée dans une connexion par une application.

## <a name="examples"></a>Exemples

L’exemple VBScript [modifier l’heure de maintien de l’activité pour toutes les cartes réseau](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) configure l’heure de maintien de l’activité pour toutes les cartes réseau d’un ordinateur à 300 000 millisecondes (5 minutes).

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

 

