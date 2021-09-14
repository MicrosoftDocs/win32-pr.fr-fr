---
title: L’en-tête
description: L’en-tête suivant représente l’un des styles d’en-tête qui peuvent être générés par la version actuelle de MIDL. Pour plus de commodité, la liste complète des champs d’en-tête est fournie ici.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afcc9ad880278fdbcb8efc45fdabdc22ad06224
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416580"
---
# <a name="the-header"></a>L’en-tête

L’en-tête suivant représente l’un des styles d’en-tête qui peuvent être générés par la version actuelle de MIDL. Pour plus de commodité, la liste complète des champs d’en-tête est fournie ici.

(-En-tête de l'[**en-tête**](/windows/desktop/Midl/-oi) )

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

Extensions à partir de Windows 2000 : <8> pour 32 bits, <12> pour 64 bits)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

La \_ version d’extension<1> fournit la taille de la section d’extension, en octets. Cela permet au moteur de NDR actuel d’effectuer un pas à pas détaillé dans la section d’extension, même si la section devait provenir d’une version ultérieure du compilateur contenant plus de champs que le moteur actuel ne comprend.

L’INTERPRÉTeur d’FLAGS2 de l’INTERPRÉTeur \_ \_ est défini comme suit :

``` syntax
typedef struct
  {
  unsigned char   HasNewCorrDesc      : 1;    // 0x01
  unsigned char   ClientCorrCheck     : 1;    // 0x02
  unsigned char   ServerCorrCheck     : 1;    // 0x04
  unsigned char   HasNotify           : 1;    // 0x08
  unsigned char   HasNotify2          : 1;    // 0x10
  unsigned char   Unused              : 3;
  } INTERPRETER_OPT_FLAGS2, *PINTERPRETER_OPT_FLAGS2;
```

Le membre **HasNewCorrDesc** indique si de nouveaux descripteurs de corrélation sont utilisés dans les chaînes de format générées par le compilateur. Le nouveau descripteur de corrélation est lié à la fonctionnalité de déni de l’attaque. Les membres **ClientCorrCheck** et **ServerCorrCheck** sont définis lorsque la routine doit vérifier la corrélation du côté indiqué.

Les indicateurs **HasNotify** et **HasNotify2** indiquent que la routine utilise la fonctionnalité Notify comme défini par les attributs **\[ notifier \]** et **\[ notifier \_ \]** , respectivement.

Le membre **ClientCorrCheck** est un indicateur de taille de cache côté client et **ServerCorrCheck** est un indicateur côté serveur. Si la taille est égale à zéro, une taille par défaut doit être utilisée.

L’élément **NotifyIndex** est un index d’une routine Notify, s’il est utilisé.

L’élément **FloatDoubleMask** traite le problème d’un argument à virgule flottante pour le Windows de 64 bits. Ce champ est généré uniquement pour les stubs 64 bits. Le masque est nécessaire pour les routines d’assembly qui téléchargent/chargent les registres à partir de/vers la pile virtuelle pour gérer les arguments à virgule flottante et s’inscrit correctement. Le masque est constitué de 2 bits par argument, ou non par registre à virgule flottante. Le codage est le suivant : les bits les moins significatifs correspondent au premier registre FP, les 2 bits suivants correspondent au deuxième Registre, et ainsi de suite.

> [!Note]  
> Pour les routines d’objet, le premier argument finit dans le deuxième Registre en raison de la première position de ce pointeur. Pour chaque registre, la signification de bits est indiquée dans le tableau suivant.

 



| Bits | Signification                                          |
|------|--------------------------------------------------|
| 01   | Une valeur flottante doit être chargée dans le registre.  |
| 10   | Une valeur double doit être chargée dans le registre. |



 

00 et 11 sont des valeurs non valides pour les bits.

Actuellement, il existe huit registres FP dans un processeur Intel 64-bit architecture. par conséquent, le masque ne peut avoir que les bits les plus faibles définis. La taille du masque a été définie sur un total de 16 bits, en fonction du masque de compilateur C restant inchangé.

## <a name="header-streamlining-for-performance"></a>En-tête simplifié pour les performances

Pour simplifier le code et améliorer les performances, le compilateur tente de générer un en-tête de taille fixe chaque fois que cela est possible. En particulier, l’en-tête suivant est utilisé pour le modèle DCOM asynchrone :

``` syntax
typedef struct _NDR_DCOM_OI2_PROC_HEADER
  {
  unsigned char               HandleType;        // The Oi header
  INTERPRETER_FLAGS           OldOiFlags;        //
  unsigned short              RpcFlagsLow;       //
  unsigned short              RpcFlagsHi;        //
  unsigned short              ProcNum;           //
  unsigned short              StackSize;         //
  // expl handle descr is never generated        //
  unsigned short              ClientBufferSize;  // The Oi2 header
  unsigned short              ServerBufferSize;  //
  INTERPRETER_OPT_FLAGS       Oi2Flags;          //
  unsigned char               NumberParams;      //
  } NDR_DCOM_OI2_PROC_HEADER, *PNDR_DCOM_OI2_PROC_HEADER;
```

 

 