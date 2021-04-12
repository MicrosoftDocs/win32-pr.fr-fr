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
# <a name="common-compiler-errors"></a><span data-ttu-id="4e80d-106">Erreurs courantes du compilateur</span><span class="sxs-lookup"><span data-stu-id="4e80d-106">Common Compiler Errors</span></span>

<span data-ttu-id="4e80d-107">Cette section illustre les erreurs de compilateur classiques qui se produisent lors de la migration d’une base de code existante.</span><span class="sxs-lookup"><span data-stu-id="4e80d-107">This section illustrates the typical compiler errors that occur when migrating an existing code base.</span></span> <span data-ttu-id="4e80d-108">Ces exemples peuvent provenir du code HAL au niveau système, bien que les concepts soient directement applicables au code au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e80d-108">These examples happen to be from system-level HAL code, although the concepts are directly applicable to user-level code.</span></span>

## <a name="warning-c4311-example-1"></a><span data-ttu-id="4e80d-109">AVERTISSEMENT C4311 exemple 1</span><span class="sxs-lookup"><span data-stu-id="4e80d-109">Warning C4311 Example 1</span></span>

<span data-ttu-id="4e80d-110">'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long</span><span class="sxs-lookup"><span data-stu-id="4e80d-110">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span data-ttu-id="4e80d-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-113">**PtrToUlong** est une fonction inline ou une macro, en fonction de votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="4e80d-113">**PtrToUlong** is an inline function or macro, depending on your usage.</span></span> <span data-ttu-id="4e80d-114">Il tronque un pointeur vers un **ULong**.</span><span class="sxs-lookup"><span data-stu-id="4e80d-114">It truncates a pointer to a **ULONG**.</span></span> <span data-ttu-id="4e80d-115">Bien que les pointeurs 32 bits ne soient pas affectés, la moitié supérieure d’un pointeur de 64 bits est tronquée.</span><span class="sxs-lookup"><span data-stu-id="4e80d-115">Although 32-bit pointers are not affected, the upper half of a 64-bit pointer is truncated.</span></span>

<span data-ttu-id="4e80d-116">L' \_ \_ \_ QVA de base de configuration PCI CIA \_ est déclaré en tant que **pVoid**.</span><span class="sxs-lookup"><span data-stu-id="4e80d-116">CIA\_PCI\_CONFIG\_BASE\_QVA is declared as a **PVOID**.</span></span> <span data-ttu-id="4e80d-117">Le Cast **ULong** fonctionne dans le monde 32 bits, mais génère une erreur dans le monde de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-117">The **ULONG** cast works in the 32-bit world, but results in an error in the 64-bit world.</span></span> <span data-ttu-id="4e80d-118">La solution consiste à obtenir un pointeur 64 bits vers **ULong**, car la modification de la définition de l’Union >pPciAddr u. AsULONG est définie dans des modifications trop nombreuses.</span><span class="sxs-lookup"><span data-stu-id="4e80d-118">The solution is to get a 64-bit pointer to a **ULONG**, because changing the definition of the union that pPciAddr->u.AsULONG is defined in changes too much code.</span></span>

<span data-ttu-id="4e80d-119">L’utilisation de la macro **PtrToUlong** pour convertir le **pVoid** 64 bits en le **ULong** requis est autorisée, car nous avons connaissance de la valeur spécifique du QVA de \_ base de configuration PCI CIA \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4e80d-119">Using the macro **PtrToUlong** to convert the 64-bit **PVOID** to the needed **ULONG** is allowed because we have knowledge about the specific value of CIA\_PCI\_CONFIG\_BASE\_QVA.</span></span> <span data-ttu-id="4e80d-120">Dans ce cas, ce pointeur n’aura jamais de données dans les 32 bits supérieurs.</span><span class="sxs-lookup"><span data-stu-id="4e80d-120">In this case, this pointer will never have data in the upper 32 bits.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a><span data-ttu-id="4e80d-122">AVERTISSEMENT C4311 exemple 2</span><span class="sxs-lookup"><span data-stu-id="4e80d-122">Warning C4311 Example 2</span></span>

<span data-ttu-id="4e80d-123">'cast de type' : troncation de pointeur de’struct \_ Error \_ frame \* \_ \_ ptr64 'à’unsigned long</span><span class="sxs-lookup"><span data-stu-id="4e80d-123">'type cast' : pointer truncation from 'struct \_ERROR\_FRAME \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span data-ttu-id="4e80d-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-126">Le problème est que le dernier paramètre de cette fonction est un pointeur vers une structure de données.</span><span class="sxs-lookup"><span data-stu-id="4e80d-126">The problem is that the last parameter to this function is a pointer to a data structure.</span></span> <span data-ttu-id="4e80d-127">Étant donné que PUncorrectableError est un pointeur, il change de taille avec le modèle de programmation.</span><span class="sxs-lookup"><span data-stu-id="4e80d-127">Because PUncorrectableError is a pointer, it changes size with the programming model.</span></span> <span data-ttu-id="4e80d-128">Le prototype de **KeBugCheckEx** a été modifié afin que le dernier paramètre soit **un \_ ptr ulong**.</span><span class="sxs-lookup"><span data-stu-id="4e80d-128">The prototype for **KeBugCheckEx** was changed so that the last parameter is a **ULONG\_PTR**.</span></span> <span data-ttu-id="4e80d-129">Par conséquent, il est nécessaire d’effectuer un cast du pointeur de fonction **en \_ ptr ulong**.</span><span class="sxs-lookup"><span data-stu-id="4e80d-129">As a result, it's necessary to cast the function pointer to a **ULONG\_PTR**.</span></span>

<span data-ttu-id="4e80d-130">Vous pouvez vous demander pourquoi **pVoid** n’a pas été utilisé en tant que dernier paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e80d-130">You might ask why **PVOID** was not used as the last parameter.</span></span> <span data-ttu-id="4e80d-131">En fonction du contexte de l’appel, le dernier paramètre peut être autre chose qu’un pointeur ou peut-être un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4e80d-131">Depending on the context of the call, the last parameter may be something other than a pointer or perhaps an error code.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a><span data-ttu-id="4e80d-133">AVERTISSEMENT C4244-exemple 1</span><span class="sxs-lookup"><span data-stu-id="4e80d-133">Warning C4244 Example 1</span></span>

<span data-ttu-id="4e80d-134">' = ' : conversion de’struct \_ configuration \_ Component \* \_ \_ ptr64 'en’struct \_ configuration \_ Component \* ', perte possible de données</span><span class="sxs-lookup"><span data-stu-id="4e80d-134">'=' : conversion from 'struct \_CONFIGURATION\_COMPONENT \*\_\_ptr64 ' to 'struct \_CONFIGURATION\_COMPONENT \*', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span data-ttu-id="4e80d-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-137">La fonction déclare le composant variable en tant que \_ composant PCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="4e80d-137">The function declares the variable Component as a PCONFIGURATION\_COMPONENT.</span></span> <span data-ttu-id="4e80d-138">Plus tard, la variable est utilisée dans l’attribution suivante qui est correcte :</span><span class="sxs-lookup"><span data-stu-id="4e80d-138">Later, the variable is used in the following assignment that appears correct:</span></span>

`Component = &CurrentEntry->ComponentEntry;`

<span data-ttu-id="4e80d-139">Toutefois, le composant type PCONFIGURATION \_ est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="4e80d-139">However, the type PCONFIGURATION\_COMPONENT is defined as:</span></span>

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

<span data-ttu-id="4e80d-140">La définition de type pour le \_ composant PCONFIGURATION fournit un pointeur 32 bits dans les modèles 32 bits et 64 bits, car il est déclaré comme **pointeur \_ 32**.</span><span class="sxs-lookup"><span data-stu-id="4e80d-140">The type definition for PCONFIGURATION\_COMPONENT provides a 32-bit pointer in both 32-bit and 64-bit models because it is declared **POINTER\_32**.</span></span> <span data-ttu-id="4e80d-141">Le concepteur d’origine de cette structure savait qu’il devait être utilisé dans un contexte 32 bits dans le BIOS et le définir expressément pour cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="4e80d-141">The original designer of this structure knew it was going to be used in a 32-bit context in the BIOS and expressly defined it for that use.</span></span> <span data-ttu-id="4e80d-142">Ce code fonctionne correctement dans Windows 32 bits, car les pointeurs se présentent sous la 32-bit.</span><span class="sxs-lookup"><span data-stu-id="4e80d-142">This code works fine in 32-bit Windows because the pointers happen to be 32-bit.</span></span> <span data-ttu-id="4e80d-143">Dans Windows 64 bits, il ne fonctionne pas, car le code est en contexte 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-143">In 64-bit Windows, it does not work because the code is in 64-bit context.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-145">Pour contourner ce problème, utilisez \_ le composant configuration \* plutôt que le composant PCONFIGURATION bits 32 \_ .</span><span class="sxs-lookup"><span data-stu-id="4e80d-145">To work around this problem, use CONFIGURATION\_COMPONENT \* rather than the 32-bit PCONFIGURATION\_COMPONENT .</span></span> <span data-ttu-id="4e80d-146">Il est important de bien comprendre l’objectif du code.</span><span class="sxs-lookup"><span data-stu-id="4e80d-146">It is important to clearly understand the purpose of the code.</span></span> <span data-ttu-id="4e80d-147">Si ce code est destiné à toucher le BIOS ou l’espace système 32 bits, ce correctif ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="4e80d-147">If this code is intended to touch 32-bit BIOS or System space, this fix will not work.</span></span>

<span data-ttu-id="4e80d-148">Le **pointeur \_ 32** est défini dans Ntdef. h et Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="4e80d-148">**POINTER\_32** is defined in Ntdef.h and Winnt.h.</span></span>

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a><span data-ttu-id="4e80d-149">AVERTISSEMENT C4242 exemple 2</span><span class="sxs-lookup"><span data-stu-id="4e80d-149">Warning C4242 Example 2</span></span>

<span data-ttu-id="4e80d-150">' = ' : conversion de' \_ \_ Int64 'en’unsigned long', perte possible de données</span><span class="sxs-lookup"><span data-stu-id="4e80d-150">'=' : conversion from '\_\_int64 ' to 'unsigned long ', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="4e80d-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-153">Cet avertissement est généré parce que le calcul utilise des valeurs 64 bits, dans ce cas des pointeurs, et en plaçant le résultat dans un **ULong** de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-153">This warning is generated because the calculation is using 64-bit values, in this case pointers, and placing the result in a 32-bit **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-155">Effectuez un cast du résultat du calcul en **ULong** comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="4e80d-155">Type cast the result of the calculation to a **ULONG** as shown here:</span></span>

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

<span data-ttu-id="4e80d-156">Cast le résultat permet au compilateur de savoir si vous êtes sûr du résultat.</span><span class="sxs-lookup"><span data-stu-id="4e80d-156">Typecasting the result lets the compiler know you are sure about the result.</span></span> <span data-ttu-id="4e80d-157">Cela dit, assurez-vous que vous comprenez le calcul et que vous êtes vraiment sûr qu’il sera contenu dans un **ULONG** 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-157">That being said, make certain you understand the calculation and really are sure it will fit in a 32-bit **ULONG**.</span></span>

<span data-ttu-id="4e80d-158">Si le résultat ne peut pas être contenu dans un **ULONG** 32 bits, modifiez le type de base de la variable qui contiendra le résultat.</span><span class="sxs-lookup"><span data-stu-id="4e80d-158">If the result may not fit in a 32-bit **ULONG**, change the base type of the variable that will hold the result.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-1"></a><span data-ttu-id="4e80d-159">AVERTISSEMENT C4311-exemple 1</span><span class="sxs-lookup"><span data-stu-id="4e80d-159">Warning C4311 - Example 1</span></span>

<span data-ttu-id="4e80d-160">'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'</span><span class="sxs-lookup"><span data-stu-id="4e80d-160">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="4e80d-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-163">Cette fonction entière traite les adresses comme des entiers, ce qui nécessite la nécessité de taper ces entiers de manière portable.</span><span class="sxs-lookup"><span data-stu-id="4e80d-163">This entire function deals with addresses as integers, necessitating the need to type those integers in a portable way.</span></span> <span data-ttu-id="4e80d-164">Toutes les variables locales, les valeurs intermédiaires dans les calculs et les valeurs de retour doivent être des types portables.</span><span class="sxs-lookup"><span data-stu-id="4e80d-164">All the local variables, intermediate values in calculations, and return values should be portable types.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
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

<span data-ttu-id="4e80d-166">**Pulong \_ PTR** est un pointeur qui est lui-même 32 bits pour windows 32 bits et 64 bits pour windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-166">**PULONG\_PTR** is a pointer that is itself 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span> <span data-ttu-id="4e80d-167">Il pointe vers un entier non signé, **ULong \_ ptr**, qui est 32 bits pour Windows 32 bits et 64 bits pour Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-167">It points to an unsigned integer, **ULONG\_PTR**, that is 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-2"></a><span data-ttu-id="4e80d-168">AVERTISSEMENT C4311-exemple 2</span><span class="sxs-lookup"><span data-stu-id="4e80d-168">Warning C4311 - Example 2</span></span>

<span data-ttu-id="4e80d-169">'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'</span><span class="sxs-lookup"><span data-stu-id="4e80d-169">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="4e80d-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-172">Même si toutes les valeurs QVA (quasi virtuelle) sont en fait des valeurs de 32 bits à ce niveau et qu’elles tiennent dans un **ULong**, il est plus cohérent de traiter toutes les adresses comme des valeurs **\_ ptr ulong** lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="4e80d-172">Even though all QVA (Quasi Virtual Address) values are really 32-bit values at this stage and will fit in a **ULONG**, it is more consistent to treat all addresses as **ULONG\_PTR** values when possible.</span></span>

<span data-ttu-id="4e80d-173">Le pointeur PciIoSpaceBase contient le QVA créé dans la couche HAL des macros \_ Make \_ QVA.</span><span class="sxs-lookup"><span data-stu-id="4e80d-173">The pointer PciIoSpaceBase holds the QVA that is created in the macro HAL\_MAKE\_QVA.</span></span> <span data-ttu-id="4e80d-174">Cette macro retourne une valeur 64 bits avec les 32 bits supérieurs ayant la valeur zéro pour que l’opération mathématique fonctionne.</span><span class="sxs-lookup"><span data-stu-id="4e80d-174">This macro returns a 64-bit value with the top 32 bits set to zero so the math will work.</span></span> <span data-ttu-id="4e80d-175">Nous pourrions simplement conserver le code pour tronquer le pointeur dans un **ULong**, mais cette pratique est déconseillée pour améliorer la maintenabilité et la portabilité du code.</span><span class="sxs-lookup"><span data-stu-id="4e80d-175">We could simply leave the code to truncate the pointer into a **ULONG**, but this practice is discouraged to enhance code maintainability and portability.</span></span> <span data-ttu-id="4e80d-176">Par exemple, le contenu d’un QVA peut changer à l’avenir pour utiliser certains bits supérieurs à ce niveau, ce qui rompt le code.</span><span class="sxs-lookup"><span data-stu-id="4e80d-176">For example, the contents of a QVA might change in the future to use some of the upper bits at this level, breaking the code.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-178">Soyez sûr et utilisez **ULong \_ ptr** pour toutes les maths d’adresse et de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4e80d-178">Be safe and use **ULONG\_PTR** for all address and pointer math.</span></span>

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a><span data-ttu-id="4e80d-179">AVERTISSEMENT C4311 exemple 3</span><span class="sxs-lookup"><span data-stu-id="4e80d-179">Warning C4311 Example 3</span></span>

<span data-ttu-id="4e80d-180">'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'</span><span class="sxs-lookup"><span data-stu-id="4e80d-180">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="4e80d-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-183">Le compilateur vous avertit des opérateurs d’adresse (&) et de décalage gauche (<<) s’ils sont appliqués à des types pointeur.</span><span class="sxs-lookup"><span data-stu-id="4e80d-183">The compiler warns about the address of (&) and left shift (<<) operators if they are applied to pointer types.</span></span> <span data-ttu-id="4e80d-184">Dans le code ci-dessus, QVA est une valeur **pVoid** .</span><span class="sxs-lookup"><span data-stu-id="4e80d-184">In the above code, Qva is a **PVOID** value.</span></span> <span data-ttu-id="4e80d-185">Nous devons effectuer un cast de ce en type entier pour effectuer les opérations mathématiques.</span><span class="sxs-lookup"><span data-stu-id="4e80d-185">We need to cast that to an integer type to perform the math.</span></span> <span data-ttu-id="4e80d-186">Étant donné que le code doit être portable, utilisez **ULong \_ ptr** au lieu de **ULong**.</span><span class="sxs-lookup"><span data-stu-id="4e80d-186">Because the code must be portable, use **ULONG\_PTR** instead of **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a><span data-ttu-id="4e80d-188">AVERTISSEMENT C4311 exemple 4</span><span class="sxs-lookup"><span data-stu-id="4e80d-188">Warning C4311 Example 4</span></span>

<span data-ttu-id="4e80d-189">'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'</span><span class="sxs-lookup"><span data-stu-id="4e80d-189">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span data-ttu-id="4e80d-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-192">TranslatedAddress est une Union qui ressemble à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="4e80d-192">TranslatedAddress is a union that looks something like the following:</span></span>

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

<span data-ttu-id="4e80d-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-194">Sachant que le reste du code peut être placé dans Highpart, nous pouvons sélectionner l’une des solutions présentées ici.</span><span class="sxs-lookup"><span data-stu-id="4e80d-194">Knowing what the rest of the code might place in Highpart, we can select either of the solutions shown here.</span></span>

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

<span data-ttu-id="4e80d-195">La macro **PtrToUlong** tronque le pointeur retourné par **HalCreateQva** à 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-195">The **PtrToUlong** macro truncates the pointer returned by **HalCreateQva** to 32 bits.</span></span> <span data-ttu-id="4e80d-196">Nous savons que le QVA retourné par **HalCreateQva** a les 32 bits supérieurs ayant la valeur zéro et que la ligne de code suivante définit TranslatedAddress->Highpart sur zéro.</span><span class="sxs-lookup"><span data-stu-id="4e80d-196">We know that the QVA returned by **HalCreateQva** has the upper 32 bits set to zero and the very next line of code sets TranslatedAddress->Highpart to zero.</span></span>

<span data-ttu-id="4e80d-197">Avec prudence, nous pourrions utiliser ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="4e80d-197">With caution, we could use the following:</span></span>

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

<span data-ttu-id="4e80d-198">Cela fonctionne dans cet exemple : la macro **HalCreateQva** retourne 64 bits, avec les 32 bits supérieurs définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="4e80d-198">This works in this example: the **HalCreateQva** macro is returning 64 bits, with the upper 32 bits set to zero.</span></span> <span data-ttu-id="4e80d-199">Veillez simplement à ne pas conserver les 32 bits supérieurs non définis dans un environnement de 32 bits, ce que cette deuxième solution peut en fait.</span><span class="sxs-lookup"><span data-stu-id="4e80d-199">Just be careful not to leave the upper 32 bits undefined in a 32-bit environment, which this second solution may actually do.</span></span>

</dd> </dl>

## <a name="warning-c4311-example-5"></a><span data-ttu-id="4e80d-200">AVERTISSEMENT C4311 exemple 5</span><span class="sxs-lookup"><span data-stu-id="4e80d-200">Warning C4311 Example 5</span></span>

<span data-ttu-id="4e80d-201">'cast de type' : troncation de pointeur de’void \* \_ \_ ptr64 'à’unsigned long'</span><span class="sxs-lookup"><span data-stu-id="4e80d-201">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="4e80d-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="4e80d-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="4e80d-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="4e80d-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="4e80d-204">WindowRegisters->WindowBase est un pointeur et est maintenant 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-204">WindowRegisters->WindowBase is a pointer and is now 64 bits.</span></span> <span data-ttu-id="4e80d-205">Le code indique de déplacer cette valeur de 20 bits vers la droite.</span><span class="sxs-lookup"><span data-stu-id="4e80d-205">The code says to right-shift this value 20 bits.</span></span> <span data-ttu-id="4e80d-206">Le compilateur ne nous permet pas d’utiliser l’opérateur de décalage vers la droite (>>) sur un pointeur. par conséquent, nous devons effectuer un cast en un type entier.</span><span class="sxs-lookup"><span data-stu-id="4e80d-206">The compiler will not let us use the right-shift (>>) operator on a pointer; therefore, we need to cast it to some sort of integer.</span></span>

</dd> <dt>

<span data-ttu-id="4e80d-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Elle</span><span class="sxs-lookup"><span data-stu-id="4e80d-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

<span data-ttu-id="4e80d-208">Le cast en **\_ ptr ulong** est exactement ce dont nous avons besoin.</span><span class="sxs-lookup"><span data-stu-id="4e80d-208">Casting to a **ULONG\_PTR** is just what we need.</span></span> <span data-ttu-id="4e80d-209">Le problème suivant est wbase.</span><span class="sxs-lookup"><span data-stu-id="4e80d-209">The next problem is Wbase.</span></span> <span data-ttu-id="4e80d-210">Wbase est de **ULong** et est 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-210">Wbase is a **ULONG** and is 32 bits.</span></span> <span data-ttu-id="4e80d-211">Dans ce cas, nous savons que le pointeur 64 bits WindowRegisters->WindowBase est valide dans les 32 bits inférieurs, même après avoir été déplacé.</span><span class="sxs-lookup"><span data-stu-id="4e80d-211">In this case, we know that the 64-bit pointer WindowRegisters->WindowBase is valid in the lower 32 bits even after being shifted.</span></span> <span data-ttu-id="4e80d-212">Cela permet d’utiliser la macro **PtrToUlong** acceptable, car elle tronque le pointeur 64 bits en **ULong** 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4e80d-212">This makes use of the **PtrToUlong** macro acceptable, because it will truncate the 64-bit pointer into a 32-bit **ULONG**.</span></span> <span data-ttu-id="4e80d-213">Le Cast **pVoid** est nécessaire, car **PtrToUlong** attend un argument de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4e80d-213">The **PVOID** cast is necessary because **PtrToUlong** expects a pointer argument.</span></span> <span data-ttu-id="4e80d-214">Lorsque vous examinez le code assembleur qui en résulte, tout ce code C est casté en une seule charge, Shift Right et Store long.</span><span class="sxs-lookup"><span data-stu-id="4e80d-214">When you look at the resulting assembler code, all this C code casting becomes just a load quad, shift right, and store long.</span></span>

</dd> </dl>

 

 




