---
description: La classe CommandLineEventConsumer démarre un processus arbitraire dans le système local lorsqu’un événement lui est remis.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: CommandLineEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106539267"
---
# <a name="commandlineeventconsumer-class"></a>CommandLineEventConsumer, classe

La classe **CommandLineEventConsumer** démarre un processus arbitraire dans le système local lorsqu’un événement lui est remis. Cette classe est l’un des consommateurs d’événements standard fournis par WMI. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

> [!Note]  
> Quand vous utilisez la classe **CommandLineEventConsumer** , sécurisez l’exécutable que vous souhaitez démarrer. Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou sécurisé à l’aide d’une liste de contrôle d’accès (ACL) forte, un utilisateur non autorisé peut remplacer votre exécutable par un exécutable malveillant. Pour plus d’informations sur les listes de contrôle d’accès, consultez la section sécurité du kit de développement logiciel (SDK) Microsoft Windows et consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a>Membres

La classe **CommandLineEventConsumer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CommandLineEventConsumer** possède les propriétés suivantes.

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Modèle de chaîne standard qui spécifie le processus à démarrer. Cette propriété peut avoir la **valeur null** et la propriété **ExecutablePath** est utilisée comme ligne de commande.

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non utilisé. Si une valeur est assignée à cette propriété, un message de suivi est généré. Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le nouveau processus est le processus racine d’un nouveau groupe de processus. Le groupe de processus comprend tous les processus qui sont des descendants de ce processus racine. L’identificateur de processus du nouveau groupe de processus est le même que cet identificateur de processus. Les groupes de processus sont utilisés par la méthode [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) pour permettre l’envoi d’un signal Ctrl + C ou CTRL + ATTN à un groupe de processus de console.

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le nouveau processus s’exécute sur une machine virtuelle DOS privée (VDM). Cela est valide uniquement lors du démarrage d’une application exécutée sur un système d’exploitation Windows 16 bits. Si la valeur est **false**, toutes les applications qui s’exécutent sur un système d’exploitation Windows 16 bits s’exécutent en tant que threads dans un VDM partagé unique. Pour plus d’informations, consultez la section Notes de cette rubrique.

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, la méthode [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) exécute le nouveau processus dans l’ordinateur virtuel dos (VDM) partagé. Cette propriété peut remplacer le commutateur DefaultSeparateVDM dans la section Windows de Win.ini si la valeur est **true**. Pour plus d’informations, consultez la section Notes de cette rubrique.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre. WMI stocke le SID de l’utilisateur qui crée une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) ou le SID d’administrateur, selon le système d’exploitation. Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**DesktopName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non utilisé. Si une valeur est affectée à cette propriété, un message de suivi est généré. Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Module à exécuter. La chaîne peut spécifier le chemin d’accès complet et le nom de fichier du module à exécuter, ou elle peut spécifier un nom partiel. Si un nom partiel est spécifié, le lecteur actif et le répertoire actif sont pris en défaut.

La propriété **ExecutablePath** peut avoir la **valeur null**. Dans ce cas, le nom du module doit être le premier jeton délimité par des espaces blancs dans la valeur de la propriété **CommandLineTemplate** . Si vous utilisez un nom de fichier long qui contient un espace, utilisez des chaînes entre guillemets pour indiquer l’emplacement où se termine le nom de fichier et les arguments commencent à clarifier le nom de fichier.

> [!Note]  
> Étant donné que la propriété **CommandLineTemplate** peut être un modèle dans lequel le module à exécuter est fourni par une variable, une propriété **ExecutablePath** **null** autorise le module spécifié dans le paramètre à exécuter, puis il est hors de votre contrôle. Définissez toujours la propriété **ExecutablePath** dans l’inscription **CommandLineEventConsumer** pour inclure l’exécutable requis, ce qui évite le remplacement par les paramètres d’événements. Si vous devez utiliser un modèle et une variable pour spécifier le module à exécuter, veillez à savoir qui dispose des privilèges d’écriture complets dans l’espace de noms.

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le texte et les couleurs d’arrière-plan initiaux si une nouvelle fenêtre de console est créée dans une application console

</dd> <dt>

**FillAttributes**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Texte initial et couleurs d’arrière-plan, si une nouvelle fenêtre de console est créée dans une application console. Cette propriété est ignorée dans une application GUI. La valeur peut être n’importe quelle combinaison des valeurs suivantes.

<dt>

1 (0x1)
</dt> <dd>

premier plan bleu

</dd> <dt>

2 (0X2)
</dt> <dd>

premier plan vert

</dd> <dt>

4 (0x4)
</dt> <dd>

premier plan rouge

</dd> <dt>

8 (0x8)
</dt> <dd>

intensité du premier plan

</dd> <dt>

16 (0x10)
</dt> <dd>

arrière-plan bleu

</dd> <dt>

32 (0x20)
</dt> <dd>

arrière-plan vert

</dd> <dt>

64 (0x40)
</dt> <dd>

arrière-plan rouge

</dd> <dt>

128 (0x80)
</dt> <dd>

intensité de l’arrière-plan

</dd> </dl>

Par exemple, les combinaisons suivantes produisent du texte rouge sur un arrière-plan blanc :


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  ou  


```mof
0x74
```



</dd> <dt>

**ForceOffFeedback**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le curseur de commentaires est forcé pendant le démarrage du processus. Le curseur normal s’affiche.

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le curseur est en mode commentaires pendant deux secondes après l’appel de [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Pendant ces deux secondes, si le processus effectue le premier appel d’interface utilisateur graphique, le système accorde cinq secondes supplémentaires au processus. Pendant ces cinq secondes, si le processus affiche une fenêtre, le système donne une autre période de cinq secondes au processus pour terminer le dessin de la fenêtre.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre, en secondes, pendant lequel le service WMI attend avant de tuer un processus 0 (zéro) indique qu’un processus ne doit pas être supprimé. Le fait de tuer un processus empêche l’exécution indéfinie d’un processus.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.

Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

File d’attente maximale pour un consommateur spécifique, en octets.

Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](key-qualifier.md)
</dt> </dl>

Nom unique d’un consommateur.

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Niveau de priorité de planification des threads de processus. La liste suivante répertorie les niveaux de priorité disponibles.

<dt>

32 (0x20)
</dt> <dd>

Indique un processus normal sans besoins de planification.

</dd> <dt>

64 (0x40)
</dt> <dd>

Indique un processus dont les threads s’exécutent uniquement lorsque le système est inactif et qui sont précédés par les threads de tout processus s’exécutant dans une classe de priorité plus élevée. Par exemple, un écran de veille. La classe de priorité Idle est héritée par les processus enfants.

</dd> <dt>

128 (0x80)
</dt> <dd>

Indique un processus qui exécute des tâches critiques de haute priorité. Les threads d’un processus de classe de priorité élevée précèdent les threads de processus de classe de priorité normale ou d’inactivité. Par exemple, la Liste des tâches, qui doit répondre rapidement lorsqu’elle est appelée par l’utilisateur, quelle que soit la charge sur le système. Soyez extrêmement vigilant lorsque vous utilisez la classe de priorité élevée, car une application liée au processeur avec une classe de priorité élevée peut utiliser presque tous les cycles disponibles.

</dd> <dt>

256 (0x100)
</dt> <dd>

Indique un processus qui a la priorité la plus élevée possible. Les threads d’un processus de classe de priorité en temps réel devancent les threads de tous les autres processus, y compris les processus du système d’exploitation qui effectuent des tâches importantes. Par exemple, un processus en temps réel qui s’exécute depuis plus d’un court intervalle peut entraîner la non-vidage du cache disque ou l’absence de réponse de la souris.

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le processus est lancé dans la fenêtre interactive. Si la **valeur est false**, le processus est lancé dans la station de service par défaut. Cette propriété remplace la propriété **DesktopName** . Cette propriété est utilisée uniquement localement, et uniquement si l’utilisateur interactif est le même utilisateur qui a configuré le consommateur.

À compter de Windows Vista, le processus qui exécute l’instance **CommandLineEventConsumer** est démarré sous le compte **LocalSystem** et est dans la session 0. Les services qui s’exécutent dans la session 0 ne peuvent pas interagir avec les sessions utilisateur.

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Affichage de l’état de la fenêtre. Il peut s’agir de l’une des valeurs qui peuvent être spécifiées dans le paramètre *nCmdShow* pour la fonction [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le mode d’erreur par défaut est utilisé.

</dd> <dt>

**WindowTitle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Titre qui apparaît dans la barre de titre du processus. Cette propriété est ignorée pour les applications GUI.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Répertoire de travail pour ce processus.

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décalage X, en pixels, entre le bord gauche de l’écran et le bord gauche de la fenêtre, si une nouvelle fenêtre est créée.

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Largeur de la mémoire tampon d’écran, dans les colonnes de caractères, si une nouvelle fenêtre de console est créée. Cette propriété est ignorée dans un processus GUI.

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Largeur, en pixels, d’une nouvelle fenêtre, si une nouvelle fenêtre est créée.

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décalage Y, en pixels, entre le bord supérieur de l’écran et le bord supérieur de la fenêtre, si une nouvelle fenêtre est créée.

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Hauteur de la mémoire tampon d’écran, en lignes de caractères, si une nouvelle fenêtre de console est créée. Cette propriété est ignorée dans un processus GUI.

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Hauteur, en pixels, de la nouvelle fenêtre, si une nouvelle fenêtre est créée.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CommandLineEventConsumer** est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .

La propriété **CreateSeparateWowVdm** indique si le nouveau processus s’exécute sur une machine virtuelle DOS privée (VDM). L’avantage de s’exécuter séparément est qu’un incident ne met fin qu’à un seul VDM. Les programmes qui s’exécutent dans des VDM distincts continuent de fonctionner normalement, et les applications Windows 16 bits qui s’exécutent dans des VDM distincts ont des files d’attente d’entrée distinctes. Cela signifie que si une application cesse de répondre momentanément, les applications dans des VDM distincts continuent de recevoir l’entrée. L’inconvénient de l’exécution séparée est qu’il faut beaucoup plus de mémoire pour le faire. Vous devez affecter à cette propriété la **valeur true** uniquement si l’utilisateur demande que des applications Windows 16 bits s’exécutent dans leur propre VDM.

> [!Note]  
> **CommandLineEventConsumer** utilise la méthode [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) en interne et transmet les propriétés **ExecutablePath** et **CommandLineTemplate** en tant que paramètres *lpApplicationName* et *lpCommandLine* . L’exemple de code format MOF (MOF) suivant n’utilise pas correctement **CommandLineEventConsumer** .

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



La méthode [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) passe *lpCommandLine* comme `argv[0]` , `argv[1]` , et ainsi de suite. Étant donné que `argv[0]` pour les applications 16 bits utilisées pour le nom de fichier exécutable, le code MOF précédent entraîne la création du processus comme si la commande suivante soit entrée à l’invite de commandes : **c : \\ Windows \\ system32 \\cscript.exe param1 param2**.

La commande précédente ne fonctionne pas, car Cscript.exe n’examine pas `argv[0]` , et ne reconnaît pas qu’elle ne contient pas son propre nom, mais autre chose (« c : \\ \\ scripts \\ \\MyScript.js »). L’exemple suivant identifie l’utilisation recommandée de **CommandLineEventConsumer**.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



L’utilisation précédente de **CommandLineEventConsumer** entraîne la création du processus comme si la commande suivante avait été entrée à l’invite de commandes : **c : \\ Windows \\ system32 \\cscript.exe c : \\ scripts \\MyScript.js param1 param2**

Étant donné que « c : \\ \\ scripts \\ \\MyScript.js » est maintenant `argv[1]` , il est visible par Cscript.exe et la commande est exécutée correctement.

Pour plus d’informations, consultez la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de **CommandLineEventConsumer** pour créer un consommateur, consultez [exécution d’un programme à partir de la ligne de commande en fonction d’un événement](running-a-program-from-the-command-line-based-on-an-event.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Abonnement racine<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de consommateur standard](standard-consumer-classes.md)
</dt> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Création d’un consommateur logique](creating-a-logical-consumer.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

