---
title: Méthode Listen
description: Méthode Listen
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196848"
---
# <a name="listen-method"></a>Méthode Listen

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Active le mode d’écoute (reconnaissance vocale) pour une période programmée.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent. ***caractères * * * * ("**_CharacterID_*_")._ *  *État* d’écoute



| Partie    | Description                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Obligatoire. Valeur booléenne qui détermine s’il faut activer ou désactiver le mode d’écoute. **True** Active le mode d’écoute. <br/> **Valeur false** Désactive le mode d’écoute.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La définition de cette méthode sur **true** active le mode d’écoute (active la reconnaissance vocale) pendant une période de temps fixe (10 secondes). Bien que vous ne puissiez pas définir la valeur du délai d’attente, vous pouvez désactiver le mode d’écoute avant l’expiration du délai d’attente. Si vous (ou un autre client) avez correctement défini le mode d’écoute sur et que vous tentez d’affecter à cette propriété la **valeur true** avant l’expiration du délai d’attente, la méthode réussit et réinitialise le délai d’attente. Toutefois, si le mode d’écoute est activé parce que l’utilisateur appuie sur la touche d’écoute, la méthode aboutit, mais le délai d’attente est ignoré et le mode d’écoute se termine en fonction de l’interaction de l’utilisateur avec la clé d’écoute.

Cette méthode réussit uniquement lorsqu’elle est appelée par le client d’entrée-actif et si les services vocaux ont été démarrés. Pour vous assurer que les services de reconnaissance vocale ont été démarrés, interrogez ou définissez les [**SRModeID**](srmodeid-property.md) ou définissez le paramètre de [**voix**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) avant d’appeler **Listen** , sinon la méthode échouera. Pour détecter la réussite de cette méthode, appelez-la en tant que fonction et elle renverra une valeur booléenne indiquant si la méthode a réussi.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



La méthode échoue également si l’utilisateur appuie sur la touche d’écoute et que vous tentez de définir **Listen** sur **false**. Toutefois, si l’utilisateur a relâché la clé d’écoute et que le mode d’écoute n’a pas dépassé le délai d’attente, elle échoue.

**Listen** échoue également si aucun moteur vocal compatible n’est disponible et correspond au paramètre [**LanguageID**](languageid-property.md) du caractère, l’utilisateur a désactivé l’entrée vocale à l’aide de la feuille de propriétés de l’agent Microsoft ou le périphérique audio est occupé.

Lorsque vous avez correctement défini cette méthode sur **true**, le serveur déclenche l’événement [**ListenStart**](listenstart-event.md) . Le serveur envoie [**ListenComplete**](listencomplete-event.md) lorsque le délai d’attente du mode d’écoute se termine ou lorsque vous définissez **Listen** sur **false**.

Cette méthode n’appelle pas automatiquement [**Stop**](stop-method.md) et joue une animation d’état d’écoute comme le fait le serveur quand vous appuyez sur la touche d’écoute. Cela vous permet de déterminer s’il faut interrompre l’animation en cours à l’aide de l’animation [**ListenStart**](listenstart-event.md) en appelant **Stop** et en lisant votre propre animation appropriée. Toutefois, le serveur appelle **Stop** et exécute une animation d’État auditif lorsqu’un énoncé utilisateur est détecté.

## <a name="see-also"></a>Voir aussi

[**Propriété LanguageID**](languageid-property.md), [**événement ListenComplete**](listencomplete-event.md), [**événement ListenStart**](listenstart-event.md)


 

