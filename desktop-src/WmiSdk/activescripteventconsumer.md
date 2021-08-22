---
description: Exécute un script prédéfini dans un langage de script arbitraire lorsqu’un événement lui est remis.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: ActiveScriptEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: acf7ef4b4207f72cbaee61c0aaad8b2279419682bdddbeb4373c36c6868b8fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557832"
---
# <a name="activescripteventconsumer-class"></a>ActiveScriptEventConsumer, classe

La classe **ActiveScriptEventConsumer** exécute un script prédéfini dans un langage de script arbitraire lorsqu’un événement lui est remis. Cette classe est l’un des consommateurs d’événements standard fournis par WMI. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



Vous pouvez configurer les performances de toutes les instances de **ActiveScriptEventConsumer** sur un système en définissant les valeurs de la propriété [**timeout**](scriptingstandardconsumersetting.md) ou **MaximumScripts** dans l’instance unique de **ScriptingStandardConsumerSetting**.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a>Membres

La classe **ActiveScriptEventConsumer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **ActiveScriptEventConsumer** possède les propriétés suivantes.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui représente l’identificateur de sécurité (SID), qui identifie de façon unique le créateur du consommateur d’événements active script. Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre, en secondes, pendant lequel le script est autorisé à s’exécuter. Si 0 (zéro), qui est la valeur par défaut, le script n’est pas arrêté.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur auquel WMI envoie des événements. Par Convention des consommateurs Microsoft standard, le consommateur de script ne peut pas être exécuté à distance. Les consommateurs tiers peuvent également utiliser cette propriété. Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

File d’attente maximale, en octets, pour le consommateur d’événements active script. Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Identificateur unique pour le consommateur d’événements. Si vous renommez le consommateur, le résultat est égal à deux consommateurs qui ont des noms différents.

</dd> <dt>

**ScriptFileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du fichier à partir duquel le texte du script est lu, ce qui constitue une alternative à la spécification du texte du script dans la propriété **ScriptText** . Cette propriété doit avoir la **valeur null** si la propriété **ScriptText** n’a pas la **valeur null**.

> [!Note]  
> Lorsque vous spécifiez le **ScriptFileName**, il est important de sécuriser l’exécutable que vous lancez. Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou sécurisé à l’aide d’une liste de contrôle d’accès (ACL) forte, n’importe qui peut remplacer l’exécutable par un autre. Pour plus d’informations sur les listes de contrôle d’accès, consultez [création d’un descripteur de sécurité (SD) pour un nouvel objet en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**ScriptingEngine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du moteur de script à utiliser, par exemple, « VBScript ». Cette propriété ne peut pas être **null**.

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Texte du script exprimé dans un langage connu du moteur de script. Cette propriété doit avoir la **valeur null** si la propriété **ScriptFileName** n’a pas la **valeur null**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette classe est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) . Il se trouve dans l’espace de noms de l' \\ abonnement racine.

Lorsque le texte d’un script est spécifié dans l’instance de consommateur d’événements, le script a accès à l’instance d’événement dans la variable d’environnement de script **TargetEvent**.

Les scripts s’exécutent dans le contexte de sécurité LocalSystem. Par mesure de sécurité, seul un administrateur système local ou un administrateur de domaine peut configurer le consommateur de script. Les droits d’accès ne sont pas vérifiés jusqu’au moment de l’exécution. Une fois le consommateur configuré, n’importe quel utilisateur peut déclencher l’événement qui provoque l’exécution du script.

L’échec du chargement du moteur de script ou de l’analyse et de la validation du script est considéré comme un échec. Les codes de retour d’erreur du script et l’arrêt du script à l’aide d’un délai d’attente sont également considérés comme des échecs.

**ScriptText** ou **ScriptFileName** ne doit pas avoir la **valeur null**. Si les deux propriétés ont la **valeur null** ou not **null**, une erreur est générée.

Lorsque WMI est exécuté en tant que service, les scripts exécutés par **ActiveScriptEventConsumer** ne génèrent pas de sortie écran. Les scripts qui utilisent **MsgBox** s’exécutent, mais ils n’affichent pas d’informations à l’écran. L’exécution du service WMI en tant que fichier exécutable n’est pas prise en charge, mais WMI autorise les scripts qui utilisent la fonction **MsgBox** à afficher la sortie ou à accepter les entrées utilisateur. aucune des méthodes fournies par l’objet [WScript](/previous-versions//at5ydy31(v=vs.85)) ne peut être utilisée, car **ActiveScriptEventConsumer** n’utilise pas Windows Script Host (WSH).

## <a name="examples"></a>Exemples

L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **ActiveScriptEventConsumer** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Espace de noms<br/>                | \\Abonnement racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de consommateur standard](standard-consumer-classes.md)
</dt> <dt>

[Exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[Création d’un consommateur logique](creating-a-logical-consumer.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)
</dt> </dl>

 

