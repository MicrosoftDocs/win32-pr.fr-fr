---
title: Erreurs courantes du compilateur
description: Cette section illustre les erreurs de compilateur classiques qui se produisent lors de la migration d’une base de code existante. Ces exemples peuvent provenir du code HAL au niveau système, bien que les concepts soient directement applicables au code au niveau de l’utilisateur.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- Erreurs du compilateur 64-programmation Windows bits
- migration de la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316805"
---
# <a name="common-compiler-errors"></a>Erreurs courantes du compilateur

Cette section illustre les erreurs de compilateur classiques qui se produisent lors de la migration d’une base de code existante. Ces exemples peuvent provenir du code HAL au niveau système, bien que les concepts soient directement applicables au code au niveau de l’utilisateur.

## <a name="warning-c4311-example-1"></a>AVERTISSEMENT C4311 exemple 1

'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

**PtrToUlong** est une fonction inline ou une macro, en fonction de votre utilisation. Il tronque un pointeur vers un **ULong**. Bien que les pointeurs 32 bits ne soient pas affectés, la moitié supérieure d’un pointeur de 64 bits est tronquée.

L' \_ \_ \_ QVA de base de configuration PCI CIA \_ est déclaré en tant que **pVoid**. Le Cast **ULong** fonctionne dans le monde 32 bits, mais génère une erreur dans le monde de 64 bits. La solution consiste à obtenir un pointeur 64 bits vers **ULong**, car la modification de la définition de l’Union >pPciAddr u. AsULONG est définie dans des modifications trop nombreuses.

L’utilisation de la macro **PtrToUlong** pour convertir le **pVoid** 64 bits en le **ULong** requis est autorisée, car nous avons connaissance de la valeur spécifique du QVA de \_ base de configuration PCI CIA \_ \_ \_ . Dans ce cas, ce pointeur n’aura jamais de données dans les 32 bits supérieurs.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>AVERTISSEMENT C4311 exemple 2

'cast de type' : troncation de pointeur de’struct \_ Error \_ frame \* \_ \_ ptr64 'à’unsigned long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Le problème est que le dernier paramètre de cette fonction est un pointeur vers une structure de données. Étant donné que PUncorrectableError est un pointeur, il change de taille avec le modèle de programmation. Le prototype de **KeBugCheckEx** a été modifié afin que le dernier paramètre soit **un \_ ptr ulong**. Par conséquent, il est nécessaire d’effectuer un cast du pointeur de fonction **en \_ ptr ulong**.

Vous pouvez vous demander pourquoi **pVoid** n’a pas été utilisé en tant que dernier paramètre. En fonction du contexte de l’appel, le dernier paramètre peut être autre chose qu’un pointeur ou peut-être un code d’erreur.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>AVERTISSEMENT C4244-exemple 1

' = ' : conversion de’struct \_ configuration \_ Component \* \_ \_ ptr64 'en’struct \_ configuration \_ Component \* ', perte possible de données

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

La fonction déclare le composant variable en tant que \_ composant PCONFIGURATION. Plus tard, la variable est utilisée dans l’attribution suivante qui est correcte :

`Component = &CurrentEntry->ComponentEntry;`

Toutefois, le composant type PCONFIGURATION \_ est défini comme suit :

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

La définition de type pour le \_ composant PCONFIGURATION fournit un pointeur 32 bits dans les modèles 32 bits et 64 bits, car il est déclaré comme **pointeur \_ 32**. Le concepteur d’origine de cette structure savait qu’il devait être utilisé dans un contexte 32 bits dans le BIOS et le définir expressément pour cette utilisation. Ce code fonctionne correctement dans Windows 32 bits, car les pointeurs se présentent sous la 32-bit. Dans Windows 64 bits, il ne fonctionne pas, car le code est en contexte 64 bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

Pour contourner ce problème, utilisez \_ le composant configuration \* plutôt que le composant PCONFIGURATION bits 32 \_ . Il est important de bien comprendre l’objectif du code. Si ce code est destiné à toucher le BIOS ou l’espace système 32 bits, ce correctif ne fonctionnera pas.

Le **pointeur \_ 32** est défini dans Ntdef. h et Winnt. h.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>AVERTISSEMENT C4242 exemple 2

' = ' : conversion de' \_ \_ Int64 'en’unsigned long', perte possible de données

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Cet avertissement est généré parce que le calcul utilise des valeurs 64 bits, dans ce cas des pointeurs, et en plaçant le résultat dans un **ULong** de 32 bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

Effectuez un cast du résultat du calcul en **ULong** comme indiqué ici :

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Cast le résultat permet au compilateur de savoir si vous êtes sûr du résultat. Cela dit, assurez-vous que vous comprenez le calcul et que vous êtes vraiment sûr qu’il sera contenu dans un **ULONG** 32 bits.

Si le résultat ne peut pas être contenu dans un **ULONG** 32 bits, modifiez le type de base de la variable qui contiendra le résultat.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>AVERTISSEMENT C4311-exemple 1

'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Cette fonction entière traite les adresses comme des entiers, ce qui nécessite la nécessité de taper ces entiers de manière portable. Toutes les variables locales, les valeurs intermédiaires dans les calculs et les valeurs de retour doivent être des types portables.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

**Pulong \_ PTR** est un pointeur qui est lui-même 32 bits pour windows 32 bits et 64 bits pour windows 64 bits. Il pointe vers un entier non signé, **ULong \_ ptr**, qui est 32 bits pour Windows 32 bits et 64 bits pour Windows 64 bits.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>AVERTISSEMENT C4311-exemple 2

'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Même si toutes les valeurs QVA (quasi virtuelle) sont en fait des valeurs de 32 bits à ce niveau et qu’elles tiennent dans un **ULong**, il est plus cohérent de traiter toutes les adresses comme des valeurs **\_ ptr ulong** lorsque cela est possible.

Le pointeur PciIoSpaceBase contient le QVA créé dans la couche HAL des macros \_ Make \_ QVA. Cette macro retourne une valeur 64 bits avec les 32 bits supérieurs ayant la valeur zéro pour que l’opération mathématique fonctionne. Nous pourrions simplement conserver le code pour tronquer le pointeur dans un **ULong**, mais cette pratique est déconseillée pour améliorer la maintenabilité et la portabilité du code. Par exemple, le contenu d’un QVA peut changer à l’avenir pour utiliser certains bits supérieurs à ce niveau, ce qui rompt le code.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

Soyez sûr et utilisez **ULong \_ ptr** pour toutes les maths d’adresse et de pointeur.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>AVERTISSEMENT C4311 exemple 3

'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Le compilateur vous avertit des opérateurs d’adresse (&) et de décalage gauche (<<) s’ils sont appliqués à des types pointeur. Dans le code ci-dessus, QVA est une valeur **pVoid** . Nous devons effectuer un cast de ce en type entier pour effectuer les opérations mathématiques. Étant donné que le code doit être portable, utilisez **ULong \_ ptr** au lieu de **ULong**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>AVERTISSEMENT C4311 exemple 4

'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

TranslatedAddress est une Union qui ressemble à ce qui suit :

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

Sachant que le reste du code peut être placé dans Highpart, nous pouvons sélectionner l’une des solutions présentées ici.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

La macro **PtrToUlong** tronque le pointeur retourné par **HalCreateQva** à 32 bits. Nous savons que le QVA retourné par **HalCreateQva** a les 32 bits supérieurs ayant la valeur zéro et que la ligne de code suivante définit TranslatedAddress->Highpart sur zéro.

Avec prudence, nous pourrions utiliser ce qui suit :

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Cela fonctionne dans cet exemple : la macro **HalCreateQva** retourne 64 bits, avec les 32 bits supérieurs définis sur zéro. Veillez simplement à ne pas conserver les 32 bits supérieurs non définis dans un environnement de 32 bits, ce que cette deuxième solution peut en fait.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>AVERTISSEMENT C4311 exemple 5

'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

WindowRegisters->WindowBase est un pointeur et est maintenant 64 bits. Le code indique de déplacer cette valeur de 20 bits vers la droite. Le compilateur ne nous permet pas d’utiliser l’opérateur de décalage vers la droite (>>) sur un pointeur. par conséquent, nous devons effectuer un cast en un type entier.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

Le cast en **\_ ptr ulong** est exactement ce dont nous avons besoin. Le problème suivant est wbase. Wbase est de **ULong** et est 32 bits. Dans ce cas, nous savons que le pointeur 64 bits WindowRegisters->WindowBase est valide dans les 32 bits inférieurs, même après avoir été déplacé. Cela permet d’utiliser la macro **PtrToUlong** acceptable, car elle tronque le pointeur 64 bits en **ULong** 32 bits. Le Cast **pVoid** est nécessaire, car **PtrToUlong** attend un argument de pointeur. Lorsque vous examinez le code assembleur qui en résulte, tout ce code C est casté en une seule charge, Shift Right et Store long.

</dd> </dl>

 

 




